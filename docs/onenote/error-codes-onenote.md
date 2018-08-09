---
title: Códigos de error (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 390df5ce-e730-470d-b6e9-0de4a3e904f8
description: En este tema se enumera los códigos de error en el modelo de objetos de OneNote 2013.
ms.openlocfilehash: 58c4d5d96182c49a1bc447c44763b9aaef1734ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816026"
---
# <a name="error-codes-onenote"></a>Códigos de error (OneNote)

En este tema se enumera los códigos de error en el modelo de objetos de OneNote 2013.
  
|**HResult**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|hrMalformedXML  <br/> |0x80042000  <br/> |El código XML no está bien formado.  <br/> |
|hrInvalidXML  <br/> |0x80042001  <br/> |El código XML no es válido.  <br/> |
|hrCreatingSection  <br/> |0x80042002  <br/> |No se pudo crear la sección.  <br/> |
|hrOpeningSection  <br/> |0x80042003  <br/> |No se pudo abrir la sección.  <br/> |
|hrSectionDoesNotExist  <br/> |0x80042004  <br/> |La sección no existe.  <br/> |
|hrPageDoesNotExist  <br/> |0x80042005  <br/> |La página no existe.  <br/> |
|hrFileDoesNotExist  <br/> |0x80042006  <br/> |El archivo no existe.  <br/> |
|hrInsertingImage  <br/> |0x80042007  <br/> |No se pudo insertar la imagen.  <br/> |
|hrInsertingInk  <br/> |0x80042008  <br/> |No se pudo insertar la entrada de lápiz.  <br/> |
|hrInsertingHtml  <br/> |0x80042009  <br/> |No se pudo insertar el código HTML.  <br/> |
|hrNavigatingToPage  <br/> |0x8004200a  <br/> |No se pudo abrir la página.  <br/> |
|hrSectionReadOnly  <br/> |0x8004200b  <br/> |La sección es de sólo lectura.  <br/> |
|hrPageReadOnly  <br/> |0x8004200c  <br/> |La página es de sólo lectura.  <br/> |
|hrInsertingOutlineText  <br/> |0x8004200d  <br/> |No se pudo insertar el texto del esquema.  <br/> |
|hrPageObjectDoesNotExist  <br/> |0x8004200e  <br/> |No existe el objeto page.  <br/> |
|hrBinaryObjectDoesNotExist  <br/> |0x8004200f  <br/> |No existe el objeto binario.  <br/> |
|hrLastModifiedDateDidNotMatch  <br/> |0x80042010  <br/> |No coincide con la fecha de última modificación.  <br/> |
|hrGroupDoesNotExist  <br/> |0x80042011  <br/> |No existe el grupo de sección.  <br/> |
|hrPageDoesNotExistInGroup  <br/> |0x80042012  <br/> |La página no existe en el grupo de sección.  <br/> |
|hrNoActiveSelection  <br/> |0x80042013  <br/> |No hay ninguna selección activa.  <br/> |
|hrObjectDoesNotExist  <br/> |0x80042014  <br/> |El objeto no existe.  <br/> |
|hrNotebookDoesNotExist  <br/> |0x80042015  <br/> |No existe el Bloc de notas.  <br/> |
|hrInsertingFile  <br/> |0x80042016  <br/> |No se pudo insertar el archivo.  <br/> |
|hrInvalidName  <br/> |0x80042017  <br/> |El nombre no es válido.  <br/> |
|hrFolderDoesNotExist  <br/> |0x80042018  <br/> |No existe la carpeta (grupo de sección).  <br/> |
|hrInvalidQuery  <br/> |0x80042019  <br/> |La consulta no es válida.  <br/> |
|hrFileAlreadyExists  <br/> |0x8004201a  <br/> |El archivo ya existe.  <br/> |
|hrSectionEncryptedAndLocked  <br/> |0x8004201b  <br/> |La sección está cifrada y bloqueada.  <br/> |
|hrDisabledByPolicy  <br/> |0x8004201c  <br/> |La acción está deshabilitada por una directiva.  <br/> |
   
||||
|:-----|:-----|:-----|
|hrNotYetSynchronized  <br/> |0x8004201d  <br/> |OneNote no se ha sincronizado contenido.  <br/> |
|hrLegacySection  <br/> |0x8004201E  <br/> |La sección está desde OneNote 2007 o versiones anteriores.  <br/> |
|hrMergeFailed  <br/> |0x8004201F  <br/> |Error en la operación de combinación.  <br/> |
|hrInvalidXMLSchema  <br/> |0x80042020  <br/> |El esquema XML no es válido.  <br/> |
|hrFutureContentLoss  <br/> |0x80042022  <br/> |Se ha producido pérdida de contenido (en futuras versiones de OneNote).  <br/> |
|hrTimeOut  <br/> |0x80042023  <br/> |La acción que se agotó el tiempo.  <br/> |
|hrRecordingInProgress  <br/> |0x80042024  <br/> |Grabación de audio está en curso.  <br/> |
|hrUnknownLinkedNoteState  <br/> |0x80042025  <br/> |El estado de la nota vinculada es desconocido.  <br/> |
|hrNoShortNameForLinkedNote  <br/> |0x80042026  <br/> |No existe ningún nombre corto para la nota vinculada.  <br/> |
|hrNoFriendlyNameForLinkedNote  <br/> |0x80042027  <br/> |No existe ningún nombre descriptivo para la nota vinculada.  <br/> |
|hrInvalidLinkedNoteUri  <br/> |0x80042028  <br/> |La nota vinculada URI no es válida.  <br/> |
|hrInvalidLinkedNoteThumbnail  <br/> |0x80042029  <br/> |La imagen en miniatura de notas vinculadas no es válido.  <br/> |
|hrImportLNTThumbnailFailed  <br/> |0x8004202A  <br/> |Error en la importación de miniatura de notas vinculadas.  <br/> |
|hrUnreadDisabledForNotebook  <br/> |0x8004202B  <br/> |El resaltado no leídos está deshabilitado para el Bloc de notas.  <br/> |
|hrInvalidSelection  <br/> |0x8004202C  <br/> |La selección no es válida.  <br/> |
|hrConvertFailed  <br/> |0x8004202D  <br/> |La conversión produjo un error.  <br/> |
|hrRecycleBinEditFailed  <br/> |0x8004202E  <br/> |No se pudo editar en la Papelera de reciclaje.  <br/> |
   
A continuación enumeran los códigos de error nuevo para 2013 de OneNote.
  
|**HResult**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|hrIMConversationTypeInvalid  <br/> |0x8004202F  <br/> |Devuelto por **UpdatePageContent** si era propiedad de nodo de la página de **IMConversationType** a un valor distinto de 0,1,2 o 3  <br/> |
|hrAppInModalUI  <br/> |0x80042030  <br/> |Un cuadro de diálogo modal está bloqueando la aplicación.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

