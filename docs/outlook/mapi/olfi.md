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
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279756"
---
# <a name="olfi"></a>OLFI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cola de estructuras de id. a largo plazo usadas por el proveedor de almacenamiento de archivos de carpetas personales (PST) para asignar un identificador de entrada para un nuevo mensaje o carpeta en modo sin conexión.
  
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

## <a name="members"></a>Miembros

 _ulVersion_
  
- Número de versión de la estructura. 
    
 _muidReserved_
  
- Este miembro está reservado para el uso interno de Outlook y no es compatible.
    
 _ulReserved_
  
- Este miembro está reservado para el uso interno de Outlook y no es compatible.
    
 _dwAlloc_
  
- El número de entradas que están disponibles para la asignación. Estas entradas comparten el mismo identificador único global (GUID).
    
 _dwNextAlloc_
  
- El número de entradas que están disponibles a continuación para la asignación. Estas entradas comparten el mismo GUID.
    
 _ltidAlloc_
  
- Estructura de id. a largo plazo, **[LTID,](ltid.md)** que identifica la entrada disponible actualmente para la asignación. La estructura de id. a largo plazo contiene un GUID y un índice que identifica un objeto en el almacén. Juntos, el GUID y el índice pueden formar un identificador de entrada único para un objeto. 
    
 _ltidNextAlloc_
  
- Estructura de id. a largo plazo que identifica la siguiente entrada disponible.
    
## <a name="remarks"></a>Comentarios

Un identificador de entrada es un identificador de entrada MAPI de 4 bytes para una carpeta o un mensaje. Para obtener más información, vea [ENTRYID](https://msdn.microsoft.com/library/ms836424).
  
Cuando un proveedor de almacén de PST asigna un identificador de entrada a un nuevo objeto, primero necesita un GUID que identifique el servidor y un índice que identifique el objeto en el almacén. Aunque el GUID no es único en todos los identificadores de entrada, el GUID y el índice combinados proporcionan una entrada única. Este GUID y el par de índice son rastreados por una estructura de identificador a largo plazo, **LTID**, que forma parte de la **estructura OLFI.** 
  
El proveedor de almacén de PST no mantiene físicamente en **OLFI** una estructura **LTID** para cada par de índice GUID. Mantiene una estructura **LTID,**  *ltidAlloc*  , para el primer par de índice GUID disponible actualmente; un recuento,  *dwAlloc*  , del número de entradas disponibles que comparten este mismo GUID; y una segunda **estructura LTID,**  *ltidNextAlloc*  , para el siguiente par de índice GUID disponible que tiene un GUID diferente. El proveedor de almacén de PST usa la **estructura OLFI** para realizar un seguimiento de los GUID y los índices que ha entregado. En un nivel virtual, el proveedor mantiene una reserva de varias estructuras **LTID** que están listas para asignarse.  *dwAlloc mantiene*  un recuento de las estructuras **LTID** disponibles. 
  
Las solicitudes de identificadores de entrada se incluyen en bloques. Cuando hay una solicitud para un bloque, el proveedor del almacén de PST comprueba si hay suficiente reserva al comparar el tamaño solicitado con  *dwAlloc*  . Si hay suficiente reserva, devuelve el GUID y el índice en  *ltidAlloc para*  la asignación. A continuación, disminuye  *dwAlloc*  en el tamaño solicitado e incrementa el índice  *en ltidAlloc*  por el tamaño solicitado. Esto prepara al proveedor de almacén de PST para asignar  *ltidAlloc*  en la siguiente solicitud para otro bloque de identificadores de entrada. Tenga en cuenta que el GUID sigue siendo el mismo para la siguiente solicitud. 
  
Si el tamaño de una solicitud es mayor que  *dwAlloc*  , el proveedor de almacén de PST intenta usar lo que tiene a continuación en reserva, como se especifica en  *dwNextAlloc*  y  *ltidNextAlloc*  . Copia  *dwNextAlloc*  y  *ltidNextAlloc*  en  *dwAlloc*  y  *ltidAlloc*  respectivamente, y establece  *dwNextAlloc*  y  *ltidNextAlloc*  en NULL. 
  
Un proveedor que encapsula el proveedor de almacén de PST debe comprobar periódicamente  *ltidNextAlloc*  para ver si es NULL. Si es así, el proveedor debe rellenarlo con un NUEVO GUID y restablecer  *dwNextAlloc*  para que se puedan asignar más identificadores de entrada. 
  
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

