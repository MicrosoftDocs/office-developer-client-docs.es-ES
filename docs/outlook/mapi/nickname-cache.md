---
title: Caché de alias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Last modified: January 30, 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334520"
---
# <a name="nickname-cache"></a>Caché de alias

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 y Microsoft Outlook 2013 interactúan con la memoria caché de alias, también conocida como "secuencia de autocompletar". La secuencia de autocompletar es donde Outlook conserva la lista de autocompletar, que es la lista de nombres que se muestra en los cuadros de edición **Para**, **Cc** y **CCO** mientras un usuario redacta un correo electrónico. En este tema se describe cómo Outlook 2007, Outlook 2010 y Outlook 2013 interactúan con la secuencia de autocompletar y también analiza el formato binario del archivo y las formas recomendadas para interactuar con la secuencia de autocompletar. 
  
Para las aplicaciones que interactúan con Outlook 2010 o Outlook 2013, la secuencia de autocompletar se almacena como una propiedad MAPI y se puede modificar con mapi o el **objeto PropertyAccessor** del mensaje. El **objeto PropertyAccessor** se expone en los modelos de Outlook 2010 o Outlook de objetos de 2013. 
  
No hay dependencias en el modelo Outlook objetos de 2007 ni en las API MAPI. Por lo tanto, las aplicaciones que realicen cambios en la secuencia de autocompletar en Outlook 2007 se pueden escribir con cualquier lenguaje de programación.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interactuar con la secuencia de autocompletar

Cuando se tiene acceso a los cuadros de edición **Para,** **Cc** o **CCO** en un mensaje, se carga la secuencia de autocompletar y se muestra la lista de nombres de usuario. Outlook interactúa con la secuencia de autocompletar de dos maneras: 
  
1. Carga de la secuencia de autocompletar 
    
2. Guardar cambios en los datos en la secuencia de autocompletar
    
Los medios para almacenar los datos de autocompletar difieren entre Outlook 2007 y Outlook 2010 o Outlook 2013 de la siguiente manera: 
  
 **Outlook 2007**
  
Para Outlook 2007, la secuencia de autocompletar se almacena en un archivo con el mismo nombre que el perfil y una extensión de .nk2. Por ejemplo, si se usa el perfil predeterminado de "outlook", el archivo se denominará "outlook.nk2". El archivo .nk2 se almacena en %APPDATA%\Microsoft\Outlook. Para obtener más información sobre el formato de archivo binario de caché de alias, [vea Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 y Outlook 2013**
  
Outlook 2010 o Outlook 2013 lee la secuencia de autocompletar de un mensaje en la tabla Contenido asociado de la Bandeja de entrada del almacén de entrega de la cuenta de correo. Este mensaje oculto tiene una clase de mensaje y un asunto de IPM.Configuration. Autocompletar. La secuencia de autocompletar se almacena en este mensaje en la propiedad PR_ROAMING_BINARYSTREAM ( Propiedad canónica[PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Los datos de autocompletar pueden almacenarse temporalmente en caché en un archivo .dat de autocompletar ubicado en %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Sin embargo, el archivo .dat es solo una memoria caché y no se usa para volver a escribir en el almacén de entrega cuando el usuario sale de Outlook 2010 o Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Carga de la secuencia de autocompletar

Outlook carga la secuencia de autocompletar cada vez que se inicializa un elemento con funcionalidad de direccionamiento. Por ejemplo, las direcciones de correo electrónico se usan en un nuevo correo, una respuesta de correo, un elemento de contacto, una solicitud de reunión, y así sucesivamente. Para cargar los datos, Outlook lee todo el contenido de la secuencia en la memoria.
  
Para las operaciones de autocompletar, Outlook interactúa exclusivamente con esta estructura en memoria durante la duración del outlook.exe proceso. Outlook solo guarda la estructura al cerrar. Consulte la siguiente sección "Guardar la secuencia de autocompletar" para obtener más información sobre este proceso.
  
## <a name="saving-the-autocomplete-stream"></a>Guardar la secuencia de autocompletar

Outlook guarda la secuencia de autocompletar al cerrarla si la lista de autocompletar ha cambiado de alguna de las siguientes maneras:
  
- Se agrega una nueva entrada de alias mediante la resolución de un nombre, la selección de un destinatario del cuadro de diálogo de la libreta de direcciones o el envío de correo a un destinatario que no estaba en la lista.
    
- Una entrada se modifica enviando correo a un destinatario existente en la lista.
    
- El usuario quita una entrada a través de la interfaz de usuario.
    
- Otros escenarios menores no son relevantes para este tema.
    
Guardar los cambios en los datos de autocompletar implica volver a escribir la estructura en memoria en una [secuencia de autocompletar](autocomplete-stream.md). Al interactuar con Outlook 2007, la secuencia se guarda en un archivo .nk2 local. Para Outlook 2010 o Outlook 2013, la secuencia de autocompletar vuelve a escribir en la tabla Contenido asociado de la Bandeja de entrada del almacén de entrega de la cuenta de correo.
  
## <a name="recommendations"></a>Recomendaciones

- Nunca modifique parcialmente la secuencia de autocompletar. La interacción admitida es 1) leer toda la secuencia de autocompletar en la memoria, 2) modificar la estructura de memoria y 3) escribir la secuencia completa en la tabla Contenido asociado de la Bandeja de entrada del almacén de entrega de la cuenta de correo (para Outlook 2010 o Outlook 2013) o en el archivo .nk2 local (Outlook 2007).
    
- No interactúe con la secuencia de autocompletar mientras Outlook se está ejecutando. Si Outlook se está ejecutando mientras modifica la secuencia, es probable que sobrescriba los cambios cuando se cierre.
    
- No escriba propiedades de tipo PT_MV_UNICODE y PR_MV_STRING8 en una secuencia de autocompletar que Microsoft Outlook 2003. Estas propiedades solo se entienden Outlook 2007, Outlook 2010 y Outlook 2013.
    
- Al desarrollar código que interactúe con Outlook 2007, se recomienda bloquear el archivo .nk2 de la modificación por otros procesos mientras lo lee y escribe con API de bloqueo de archivos estándar (por ejemplo, **LockFile** en C/C++ y **FileStream.Lock** en C#). 
    
- Solo modifique las propiedades de los tipos que son del conjunto de filas de la secuencia de autocompletar. Para obtener más información acerca de las propiedades de secuencia de autocompletar y los tipos de propiedades, vea [Autocomplete Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Vea también



[Secuencia de autocompletar](autocomplete-stream.md)
  
[Perfiles MAPI](mapi-profiles.md)


[Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

