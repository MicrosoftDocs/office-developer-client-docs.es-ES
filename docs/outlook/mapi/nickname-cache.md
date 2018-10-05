---
title: Caché de sobrenombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Última modificación: 30 de enero de 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389263"
---
# <a name="nickname-cache"></a>Caché de sobrenombre

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 y Microsoft Outlook 2013 interactúan con la caché de sobrenombres, también conocida como la "Autocompletar secuencia." La secuencia de Autocompletar es donde Outlook persiste la lista de Autocompletar, que es la lista de nombres que se muestra en el cuadro **para**, **Cc**, **CCO** cuadros de edición y mientras un usuario está redactando un correo electrónico. En este tema se describe cómo Outlook 2007, Outlook 2010 y Outlook 2013 interactúan con la secuencia de Autocompletar y también se describe el formato binario del archivo y los métodos recomendados para interactuar con la secuencia de Autocompletar. 
  
Para las aplicaciones que interactúan con Outlook 2010 o Outlook 2013, la secuencia de Autocompletar se almacena como una propiedad MAPI y puede modificarse mediante el objeto **PropertyAccessor** del mensaje o la MAPI. El objeto **PropertyAccessor** se expone en los modelos de objetos de Outlook 2010 o Outlook 2013. 
  
No hay ninguna dependencia en el modelo de objetos de Outlook 2007 o las API de MAPI. Por lo tanto, se pueden escribir aplicaciones que realizar cambios en la secuencia de Autocompletar en Outlook 2007 utilizando cualquier lenguaje de programación.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interactuar con la secuencia de Autocompletar

Cuando se tiene acceso a los cuadros de edición **para**, **Cc**o **CCO** de un mensaje, se carga la secuencia de Autocompletar y se muestra la lista de nombres de usuario. Outlook interactúa con la secuencia de Autocompletar de dos maneras: 
  
1. Carga de la secuencia de Autocompletar 
    
2. Guardar los cambios a los datos de la secuencia de Autocompletar
    
Los medios de almacenamiento de los datos de Autocompletar difiere entre Outlook 2007 y Outlook 2010 o Outlook 2013 como sigue: 
  
 **Outlook 2007**
  
Para Outlook 2007, la secuencia de Autocompletar se almacena en un archivo con el mismo nombre que el perfil y una extensión. nk2. Por ejemplo, si se usa el perfil predeterminado de "outlook", el archivo se llamará "outlook.nk2". El archivo. nk2 se almacena en % APPDATA%\Microsoft\Outlook. Para obtener más información sobre el formato de archivo binario de la memoria caché de alias, vea [formato de archivo de Outlook 2003/2007 NK2 y las directrices del desarrollador](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 y Outlook 2013**
  
Outlook 2010 o Outlook 2013 lee la secuencia de Autocompletar de un mensaje en la tabla de contenido asociados de la Bandeja de entrada del almacén de entrega de la cuenta de correo. Este mensaje oculto tiene una clase de mensaje y el asunto de IPM. Configuration.Autocomplete. La secuencia de Autocompletar se almacena en este mensaje en la propiedad PR_ROAMING_BINARYSTREAM ([Propiedad canónico PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Los datos de Autocompletar es posible que se almacenan temporalmente en caché en un archivo .dat de Autocompletar que se encuentra en % USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Sin embargo, el archivo .dat es sólo una memoria caché y no se usa para escribir en el almacén de entrega cuando el usuario sale de Outlook 2010 o Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Carga de la secuencia de Autocompletar

Outlook carga la secuencia de Autocompletar siempre que se inicializa un elemento con la funcionalidad de asignación de direcciones. Por ejemplo, direcciones de correo electrónico se usan en un nuevo correo, una respuesta de correo, un elemento de contacto, una convocatoria de reunión y así sucesivamente. Para cargar los datos, Outlook lee todo el contenido de la secuencia en la memoria.
  
Para las operaciones de Autocompletar, Outlook interactúa exclusivamente con esta estructura en la memoria para la duración de la duración del proceso outlook.exe. Outlook guarda únicamente la estructura en el cierre. Vea la siguiente sección "Guardar la secuencia de Autocompletar" para obtener más información acerca de este proceso.
  
## <a name="saving-the-autocomplete-stream"></a>Guardar la secuencia de Autocompletar

Outlook guarda la secuencia de Autocompletar en el cierre si ha cambiado la lista de Autocompletar en cualquiera de las siguientes maneras:
  
- Se agrega una nueva entrada de alias a través de resolución de un nombre, selección de un destinatario desde el cuadro de diálogo de la libreta de direcciones o enviar correo a un destinatario que no estaba ya en la lista.
    
- Se modifica una entrada mediante el envío de correo a un destinatario existente en la lista.
    
- Una entrada se ha quitado el usuario a través de la interfaz de usuario.
    
- Otros escenarios secundarias no se ajusten a este tema.
    
Guardar los cambios a los datos de Autocompletar implica la escritura de la estructura en la memoria en una [secuencia de Autocompletar](autocomplete-stream.md). Al interactuar con Outlook 2007, la secuencia se guarda en un archivo. nk2 local. Para Outlook 2010 o Outlook 2013, la secuencia de Autocompletar vuelve a escribe en la tabla de contenido asociados de la Bandeja de entrada del almacén de entrega de la cuenta de correo.
  
## <a name="recommendations"></a>Recomendaciones

- Nunca parcialmente, modifique la secuencia de Autocompletar. La interacción compatible es (1) lee la secuencia de Autocompletar todo en la memoria, (2) modificar la estructura de memoria y (3) escribir toda la secuencia en uno en la tabla de contenido asociados de la Bandeja de entrada del almacén de entrega de la cuenta de correo (para Outlook 2010 o Outlook 2013) o en el archivo. nk2 local (Outlook 2007).
    
- No interactúan con la secuencia de Autocompletar mientras se está ejecutando Outlook. Si Outlook se está ejecutando mientras modifica la secuencia, es probable que se sobrescribirán los cambios cuando se apaga.
    
- Escriba no propiedades de escritura de PT_MV_UNICODE y PR_MV_STRING8 en una secuencia de Autocompletar para ser consumido por Microsoft Outlook 2003. Estas propiedades sólo se entienden por Outlook 2007, Outlook 2010 y Outlook 2013.
    
- Al desarrollar código que interactúe con Outlook 2007, se recomienda bloquear el archivo. nk2 de modificación por otros procesos mientras están de lectura y escritura mediante las API (por ejemplo, **archivo de bloqueo** en C o C++ y **de bloqueo de archivos estándar FileStream.Lock** en C#). 
    
- Sólo modificar las propiedades de los tipos que están en el conjunto de filas de la secuencia de Autocompletar. Para obtener más información acerca de las propiedades de la secuencia de Autocompletar y tipos de propiedades, vea [secuencia de Autocompletar](autocomplete-stream.md).
    
## <a name="see-also"></a>Vea también



[Secuencia de Autocompletar](autocomplete-stream.md)
  
[Perfiles de MAPI](mapi-profiles.md)


[Formato de archivo de Outlook 2003/2007 NK2 y directrices para desarrolladores](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

