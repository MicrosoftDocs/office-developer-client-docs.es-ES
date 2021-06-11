---
title: Códigos de error (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 390df5ce-e730-470d-b6e9-0de4a3e904f8
description: En este tema se enumeran los códigos de error del OneNote de objetos de 2013.
ms.openlocfilehash: 83f8ad3d686693c82db1e57b8e37fa21ad140ab9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409429"
---
# <a name="error-codes-onenote"></a>Códigos de error (OneNote)

En este tema se enumeran los códigos de error del OneNote de objetos de 2013.
  
|**HResult**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|hrMalformedXML  <br/> |0x80042000  <br/> |El XML no está bien formado.  <br/> |
|hrInvalidXML  <br/> |0x80042001  <br/> |El XML no es válido.  <br/> |
|hrCreatingSection  <br/> |0x80042002  <br/> |No se pudo crear la sección.  <br/> |
|hrOpeningSection  <br/> |0x80042003  <br/> |No se pudo abrir la sección.  <br/> |
|hrSectionDoesNotExist  <br/> |0x80042004  <br/> |La sección no existe.  <br/> |
|hrPageDoesNotExist  <br/> |0x80042005  <br/> |La página no existe.  <br/> |
|hrFileDoesNotExist  <br/> |0x80042006  <br/> |El archivo no existe.  <br/> |
|hrInsertingImage  <br/> |0x80042007  <br/> |No se pudo insertar la imagen.  <br/> |
|hrInsertingInk  <br/> |0x80042008  <br/> |No se pudo insertar la tinta.  <br/> |
|hrInsertingHtml  <br/> |0x80042009  <br/> |No se pudo insertar el CÓDIGO HTML.  <br/> |
|hrNavigatingToPage  <br/> |0x8004200a  <br/> |No se pudo abrir la página.  <br/> |
|hrSectionReadOnly  <br/> |0x8004200b  <br/> |La sección es de solo lectura.  <br/> |
|hrPageReadOnly  <br/> |0x8004200c  <br/> |La página es de solo lectura.  <br/> |
|hrInsertingOutlineText  <br/> |0x8004200d  <br/> |No se pudo insertar el texto del esquema.  <br/> |
|hrPageObjectDoesNotExist  <br/> |0x8004200e  <br/> |El objeto page no existe.  <br/> |
|hrBinaryObjectDoesNotExist  <br/> |0x8004200f  <br/> |El objeto binario no existe.  <br/> |
|hrLastModifiedDateDidNotMatch  <br/> |0x80042010  <br/> |La última fecha de modificación no coincide.  <br/> |
|hrGroupDoesNotExist  <br/> |0x80042011  <br/> |El grupo de secciones no existe.  <br/> |
|hrPageDoesNotExistInGroup  <br/> |0x80042012  <br/> |La página no existe en el grupo de secciones.  <br/> |
|hrNoActiveSelection  <br/> |0x80042013  <br/> |No hay ninguna selección activa.  <br/> |
|hrObjectDoesNotExist  <br/> |0x80042014  <br/> |El objeto no existe.  <br/> |
|hrNotebookDoesNotExist  <br/> |0x80042015  <br/> |El bloc de notas no existe.  <br/> |
|hrInsertingFile  <br/> |0x80042016  <br/> |No se pudo insertar el archivo.  <br/> |
|hrInvalidName  <br/> |0x80042017  <br/> |El nombre no es válido.  <br/> |
|hrFolderDoesNotExist  <br/> |0x80042018  <br/> |La carpeta (grupo de secciones) no existe.  <br/> |
|hrInvalidQuery  <br/> |0x80042019  <br/> |La consulta no es válida.  <br/> |
|hrFileAlreadyExists  <br/> |0x8004201a  <br/> |El archivo ya existe.  <br/> |
|hrSectionEncryptedAndLocked  <br/> |0x8004201b  <br/> |La sección está cifrada y bloqueada.  <br/> |
|hrDisabledByPolicy  <br/> |0x8004201c  <br/> |La acción está deshabilitada por una directiva.  <br/> |
   
||||
|:-----|:-----|:-----|
|hrNotYetSynchronized  <br/> |0x8004201d  <br/> |OneNote aún no ha sincronizado el contenido.  <br/> |
|hrLegacySection  <br/> |0x8004201E  <br/> |La sección es de OneNote 2007 o anterior.  <br/> |
|hrMergeFailed  <br/> |0x8004201F  <br/> |Error en la operación de combinación.  <br/> |
|hrInvalidXMLSchema  <br/> |0x80042020  <br/> |El esquema XML no es válido.  <br/> |
|hrFutureContentLoss  <br/> |0x80042022  <br/> |Se ha producido una pérdida de contenido (a partir de versiones futuras de OneNote).  <br/> |
|hrTimeOut  <br/> |0x80042023  <br/> |La acción ha pasado el tiempo de espera.  <br/> |
|hrRecordingInProgress  <br/> |0x80042024  <br/> |La grabación de audio está en curso.  <br/> |
|hrUnknownLinkedNoteState  <br/> |0x80042025  <br/> |El estado de la nota vinculada es desconocido.  <br/> |
|hrNoShortNameForLinkedNote  <br/> |0x80042026  <br/> |No existe ningún nombre corto para la nota vinculada.  <br/> |
|hrNoFriendlyNameForLinkedNote  <br/> |0x80042027  <br/> |No existe ningún nombre descriptivo para la nota vinculada.  <br/> |
|hrInvalidLinkedNoteUri  <br/> |0x80042028  <br/> |El URI de la nota vinculada no es válido.  <br/> |
|hrInvalidLinkedNoteThumbnail  <br/> |0x80042029  <br/> |La miniatura de la nota vinculada no es válida.  <br/> |
|hrImportLNTThumbnailFailed  <br/> |0x8004202A  <br/> |Error en la importación de miniatura de nota vinculada.  <br/> |
|hrUnreadDisabledForNotebook  <br/> |0x8004202B  <br/> |El resaltado no leído está deshabilitado para el bloc de notas.  <br/> |
|hrInvalidSelection  <br/> |0x8004202C  <br/> |La selección no es válida.  <br/> |
|hrConvertFailed  <br/> |0x8004202D  <br/> |Error en la conversión.  <br/> |
|hrRecycleBinEditFailed  <br/> |0x8004202E  <br/> |Error de edición en la Papelera de reciclaje.  <br/> |
   
A continuación se enumeran los nuevos códigos de error OneNote 2013.
  
|**HResult**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|hrIMConversationTypeInvalid  <br/> |0x8004202F  <br/> |Devuelto por **UpdatePageContent** si la propiedad de nodo de página **IMConversationType** tenía un valor distinto de 0,1,2 o 3  <br/> |
|hrAppInModalUI  <br/> |0x80042030  <br/> |Un cuadro de diálogo modal bloquea la aplicación.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)

