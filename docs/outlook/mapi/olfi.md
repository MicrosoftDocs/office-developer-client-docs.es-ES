---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7d01f07b5eb5ca34b4bd825b62b7d1520b853d6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564265"
---
# <a name="olfi"></a>OLFI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cola de estructuras de identificador a largo plazo utilizado por el proveedor de almacén de carpetas personales (PST) para asignar un identificador de entrada para un nuevo mensaje o una carpeta en modo sin conexión.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>Members

 _ulVersion_
  
- Número de versión de la estructura. 
    
 _muidReserved_
  
- Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 _ulReserved_
  
- Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 _dwAlloc_
  
- El número de entradas que están disponibles para la asignación. Estas entradas comparten el mismo identificador único global (GUID).
    
 _dwNextAlloc_
  
- El número de entradas que están disponibles a continuación para la asignación. Estas entradas comparten el mismo GUID.
    
 _ltidAlloc_
  
- A largo plazo ID estructura, **[LTID](ltid.md)**, que identifica la entrada actualmente disponible para la asignación. La estructura de identificador a largo plazo contiene un GUID y un índice que identifica un objeto en el almacén. Juntos, el GUID y el índice pueden forman un identificador único de entrada para un objeto. 
    
 _ltidNextAlloc_
  
- Estructura de identificador que identifica la siguiente entrada disponible a largo plazo.
    
## <a name="remarks"></a>Comentarios

Un identificador de entrada es un identificador de entrada MAPI de 4 bytes para una carpeta o un mensaje. Para obtener más información, vea la [propiedad ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).
  
Cuando un proveedor de almacén de archivos PST, asigna un identificador de entrada a un nuevo objeto, primero necesita un GUID que identifica el servidor y un índice que identifica el objeto en el almacén. Aunque el GUID no es único entre todos los identificadores de entrada, el GUID y el índice combinado proporcionan una única entrada. Este par GUID y el índice se realiza un seguimiento por una estructura de identificador a largo plazo, **LTID**, que forma parte de la estructura **OLFI** . 
  
El proveedor de almacén de archivos PST no físicamente tenga en **OLFI** una estructura **LTID** para cada pareja de índice del GUID. Mantiene una estructura **LTID** , *ltidAlloc* , para el primer actualmente par GUID-índice disponible; un recuento, *dwAlloc* , el número de entradas disponibles que comparten este mismo GUID; y una segunda estructura **LTID** , *ltidNextAlloc* , para el siguiente par GUID-índice disponible que tiene un GUID diferente. El archivo PST almacenar proveedor usa la estructura **OLFI** para realizar un seguimiento de los GUID y los índices que ha entregar. En un nivel virtual, el proveedor mantiene una reserva de un número de estructuras **LTID** que están listos para ser asignado.  *dwAlloc* mantiene un recuento de las estructuras **LTID** disponibles. 
  
Las solicitudes de los identificadores de entrada se incluyen en bloques. Cuando hay una solicitud de un bloque, el proveedor de almacén de archivos PST comprueba si hay suficiente reserva por parte comparando el tamaño solicitado con *dwAlloc* . Si no hay suficiente reserva, devuelve el GUID y el índice en *ltidAlloc* para la asignación. A continuación, se disminuye *dwAlloc* por el tamaño solicitado y se incrementa el índice en *ltidAlloc* en el tamaño solicitado. Esto prepara el proveedor de almacenamiento de PST asignar *ltidAlloc* en la siguiente solicitud para otro bloque de los identificadores de entrada. Tenga en cuenta que el GUID sigue siendo la misma para la solicitud siguiente. 
  
Si el tamaño de una solicitud es mayor que *dwAlloc* , el proveedor de almacén de archivos PST intenta usar qué tiene a continuación en reserva, tal como se especifica por *dwNextAlloc* y *ltidNextAlloc* . Copia *dwNextAlloc* y *ltidNextAlloc* en *dwAlloc* y *ltidAlloc* , respectivamente y *dwNextAlloc* y *ltidNextAlloc* se establece en NULL. 
  
Un proveedor que se ajusta el proveedor de almacén de archivos PST debe comprobar periódicamente *ltidNextAlloc* para ver si es NULL. Si es así, el proveedor debe rellenar con un nuevo GUID y restablecer *dwNextAlloc* de modo que se pueden asignar más identificadores de entrada. 
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

