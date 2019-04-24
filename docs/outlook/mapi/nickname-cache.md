---
title: Caché de alias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Última modificación: 30 de enero de 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334520"
---
# <a name="nickname-cache"></a>Caché de alias

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 y Microsoft Outlook 2013 interactúan con la caché de sobrenombres, también conocida como "secuencia de autocompletar". La secuencia de autocompletar es el lugar donde Outlook conserva la lista Autocompletar, que es la lista de nombres que se muestran en los cuadros de edición **para**, **CC**y **CCO** mientras un usuario redacta un correo electrónico. En este tema se describe cómo Outlook 2007, Outlook 2010 y Outlook 2013 interactúan con la secuencia de autocompletar, así como el formato binario del archivo y los métodos recomendados para interactuar con la secuencia de autocompletar. 
  
Para las aplicaciones que interactúan con Outlook 2010 o Outlook 2013, la secuencia de autocompletar se almacena como una propiedad MAPI y se puede modificar mediante MAPI o el objeto **PropertyAccessor** del mensaje. El objeto **PropertyAccessor** se expone en los modelos de objetos Outlook 2010 o Outlook 2013. 
  
No hay ninguna dependencia en el modelo de objetos de Outlook 2007 o en las API de MAPI. Por lo tanto, las aplicaciones que realizan cambios en la secuencia de autocompletar en Outlook 2007 pueden escribirse con cualquier lenguaje de programación.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interacción con la secuencia de autocompletar

Cuando se tiene acceso a los cuadros de edición **para**, **CC**o **CCO** en un mensaje, se carga la secuencia de autocompletar y se muestra la lista de nombres de usuario. Outlook interactúa con la secuencia de autocompletar de dos maneras: 
  
1. Cargar la secuencia de autocompletar 
    
2. Guardar los cambios realizados en los datos de la secuencia de autocompletar
    
Los medios para almacenar los datos de autocompletar difieren entre Outlook 2007 y Outlook 2010 o Outlook 2013 de la siguiente manera: 
  
 **Outlook 2007**
  
Para Outlook 2007, la secuencia de autocompletar se almacena en un archivo con el mismo nombre que el perfil y una extensión de. NK2. Por ejemplo, si se usa el perfil predeterminado de "Outlook", el archivo se llamará "Outlook. NK2". El archivo. NK2 se almacena en%APPDATA%\Microsoft\Outlook. Para obtener más información acerca del formato de archivo binario de caché de sobrenombres, consulte [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 y Outlook 2013**
  
Outlook 2010 o Outlook 2013 lee la secuencia de autocompletar de un mensaje en la tabla de contenido asociada de la bandeja de entrada del almacén de entrega de la cuenta de correo. Este mensaje oculto tiene una clase de mensaje y un asunto de IPM. Configuration. AutoComplete. La secuencia de autocompletar se almacena en este mensaje en la propiedad PR_ROAMING_BINARYSTREAM ([propiedad canónica PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Los datos de autocompletar se pueden almacenar en caché temporalmente en un archivo. dat de autocompletar ubicado en%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Sin embargo, el archivo. dat es solo una caché y no se usa para volver a escribir en el almacén de entrega cuando el usuario sale de Outlook 2010 o Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Cargar la secuencia de autocompletar

Outlook carga la secuencia de autocompletar cada vez que se inicializa un elemento con funcionalidad de direccionamiento. Por ejemplo, las direcciones de correo electrónico se usan en un nuevo correo, una respuesta de correo, un elemento de contacto, una convocatoria de reunión, etc. Para cargar los datos, Outlook Lee todo el contenido de la secuencia en la memoria.
  
Para las operaciones de autocompletar, Outlook interactúa exclusivamente con esta estructura en memoria durante toda la duración del proceso de Outlook. exe. Outlook solo guarda la estructura al cerrar. Consulte la siguiente sección, "guardar la secuencia de autocompletar" para obtener más información sobre este proceso.
  
## <a name="saving-the-autocomplete-stream"></a>Guardar la secuencia de autocompletar

Outlook guarda la secuencia de autocompletar al cerrar si la lista de autocompletar ha cambiado de alguna de las maneras siguientes:
  
- Se agrega una nueva entrada de sobrenombres mediante la resolución de un nombre, la selección de un destinatario desde el cuadro de diálogo de la libreta de direcciones o el envío de correo a un destinatario que ya no estaba en la lista.
    
- Una entrada se modifica mediante el envío de correo a un destinatario existente de la lista.
    
- El usuario quita una entrada de la interfaz de usuario.
    
- Otros escenarios menores no relevantes para este tema.
    
Para guardar los cambios en los datos de autocompletar, es necesario escribir la estructura en memoria de nuevo en una [secuencia](autocomplete-stream.md)de autocompletar. Al interactuar con Outlook 2007, la secuencia se guarda en un archivo. NK2 local. Para Outlook 2010 o Outlook 2013, la secuencia de autocompletar vuelve a escribir en la tabla de contenido asociada de la bandeja de entrada del almacén de entrega de la cuenta de correo.
  
## <a name="recommendations"></a>Recomendaciones

- Nunca modifique parcialmente la secuencia de autocompletar. La interacción admitida es de 1) leer toda la secuencia de autocompletar en la memoria, 2) modifique la estructura de la memoria y 3) escriba toda la secuencia de nuevo en la tabla de contenido asociada de la bandeja de entrada del almacén de entrega de la cuenta de correo (para Outlook 2010 o Outlook 2013) o en el archivo. NK2 local (Outlook 2007).
    
- No interactúe con la secuencia de autocompletar mientras se ejecuta Outlook. Si Outlook se está ejecutando mientras modifica la secuencia, probablemente sobrescribirá los cambios cuando se cierre.
    
- No escriba propiedades de tipo PT_MV_UNICODE y PR_MV_STRING8 en una secuencia de Autocompletar para que la consuma Microsoft Outlook 2003. Estas propiedades solo se entienden en Outlook 2007, Outlook 2010 y Outlook 2013.
    
- Al desarrollar código que interactúe con Outlook 2007, se recomienda bloquear el archivo. NK2 de modificación por parte de otros procesos mientras lo lee y escribe mediante API de bloqueo de archivos estándar (por ejemplo, **LockFile** en C/C++ y ** FileStream. Lock** en C#). 
    
- Modifique solo las propiedades de los tipos que provienen del conjunto de filas de la secuencia de autocompletar. Para obtener más información acerca de las propiedades de la secuencia de autocompletar y los tipos de propiedades, consulte [secuencia](autocomplete-stream.md)de autocompletar.
    
## <a name="see-also"></a>Vea también



[Secuencia de autocompletar](autocomplete-stream.md)
  
[Perfiles MAPI](mapi-profiles.md)


[Formato de archivo de Outlook 2003/2007 NK2 y directrices para desarrolladores](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

