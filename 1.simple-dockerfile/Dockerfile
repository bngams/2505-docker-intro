# 1. Choisir l'image ou disons "template"
# FROM <image_existant>
FROM python:3.13.3-alpine3.21 

# 2. Installer l'application 

# Home dir
# WORKDIR /app

# Insérer des fichiers "dans l'image"
# COPY <host_source> <image_dest>

# Copie etape par etape 
# COPY index.py index.py
# COPY requirements.txt requirements.txt

# ou copie globale
# /!\ pê des fichiers à ignorer => .dockerignore 
# COPY . .

# ordre optimisé pour cache
COPY requirements.txt requirements.txt

# Exécuter une commande "dans l'image"
# RUN make ...
RUN pip install -r requirements.txt

# Copie apres le pip install pour conservation en cache
COPY index.py index.py

# INFO / DOC
# ne suffit pas/plus à ouvir depuis docker v.X
# server port 
EXPOSE 5000 

# 3. Instructions pour le lancement du process
# CMD['python', 'index.py'  ...] 
# python index.py
CMD ["python","index.py"]


