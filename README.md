# stack-up-the-mismatch

import os

def createIfNotExist(folder):
  if not os.path.exists('folder'):
    os.makedirs('folder')


def move(folderName , files):
    for media in medias:
       os.replace(file, f"{folderName}/{file}")
files = os.listdir()
files.remove("main.py")
print(files)
createIfNotExist('Images')
createIfNotExist('Docs')
createIfNotExist('Media')
createIfNotExist('others')

imgExts = [".png" , ".jpg" , ".jpeg"]
images = [file for file in files if os.path.splitext(file)[1].lower() in imgExts ]

docExts = [".txt" , ".docs" , "doc", ".pdf" ]
docs = [file for file in files if os.path.splitext(file)[1].lower() in docExts]
print(docs)

mediaExts= [".mp4" , ".mp3" , ".flv" ]
medias = [file for file in files if os.path.splitext(file)[1].lower() in mediaExts]

others = []
for file in files:
    ext = os.path.splitext(file)[1].lower()
    if (ext not in mediaExts) and (ext not in docsExts) and (ext not in imgExts) and os.path.isfile(file):
        others.append(file)
        
move("Images" , images)
move("Docs" , docs)
move("Media" , medias)
move("Media" , medias)
