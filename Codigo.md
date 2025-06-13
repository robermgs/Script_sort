import os
import shutil


def organizar_descargas():
    carpeta_descargas = os.path.join(os.path.expanduser("~"), "Downloads")
    subcarpetas = {
        "Documents": [".pdf", ".docx", ".xlsx", ".pptx", ".txt", ".doc", ".ppt", ".pps"],
        "Images": [".jpg", ".jpeg", ".png", ".gif"],
        "Video": [".mp4", ".mov", ".avi", ".mpg", ".mpe", ".mpeg", ".asf", ".wmv",".qt", ".rm", ".flv", ".m4v", ".webm", ".ogv", ".ogg", ".mkv", ".ts", ".tsv"],
        "Programs": [".exe", ".msi"],
        "Compressed": [".zip", ".rar", ".r0", ".r1", ".arj", ".gz", ".sit", ".sitx", ".sea", ".ace", ".bz2", ".7z"],
        "Music": [".mp3", ".wav", ".wma", ".mpa", ".ram", ".ra", ".aac", ".aif", ".m4a", ".tsa"],
        "Others": [".iso"]
    }

    for archivo in os.listdir(carpeta_descargas):
        ruta_archivo = os.path.join(carpeta_descargas, archivo)

        if os.path.isfile(ruta_archivo):
            extension = os.path.splitext(archivo)[1].lower()
            movido = False

            for subcarpeta, extensiones in subcarpetas.items():
                if extension in extensiones:
                    carpeta_destino = os.path.join(carpeta_descargas, subcarpeta)
                    os.makedirs(carpeta_destino, exist_ok=True)
                    shutil.move(ruta_archivo, os.path.join(carpeta_destino, archivo))
                    movido = True
                    break

            if not movido:
                carpeta_destino = os.path.join(carpeta_descargas, "Otros")
                os.makedirs(carpeta_destino, exist_ok=True)
                shutil.move(ruta_archivo, os.path.join(carpeta_destino, archivo))


if __name__ == "__main__":
    organizar_descargas()
