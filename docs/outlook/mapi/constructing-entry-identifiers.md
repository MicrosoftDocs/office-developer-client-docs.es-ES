---
title: Construcción de identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427951"
---
# <a name="constructing-entry-identifiers"></a>Construcción de identificadores de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los identificadores de entrada se construyen con la [estructura ENTRYID.](entryid.md) La **estructura ENTRYID** se compone de una marca que describe los atributos del identificador de entrada y el identificador de entrada real. 
  
## <a name="entryid-structure"></a>ESTRUCTURA ENTRYID

La **estructura ENTRYID** se define de la siguiente manera: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM es una constante que se define en el archivo de encabezado MapiDefs.h. 
  
El primer byte del miembro **abFlags** de 4 bytes describe el tipo y el uso del identificador de entrada y puede tener los siguientes valores: 
  
- MAPI_NOTRECI: indica que el identificador de entrada no se puede usar como destinatario en un mensaje.
    
- MAPI_NOTRESERVED: indica que otros usuarios no pueden acceder al identificador de entrada.
    
- MAPI_NOW: indica que el identificador de entrada no se puede usar en otras ocasiones.
    
- MAPI_SHORTTERM: indica que el identificador de entrada es a corto plazo. Todos los demás valores de este byte deben establecerse a menos que se permita otro uso del identificador de entrada.
    
- MAPI_THISSESSION: indica que el identificador de entrada no se puede usar en otras sesiones.
    
- MAPI_NOTRESERVED: indica que otros proveedores de servicios pueden usar el identificador de entrada para otros objetos.
    
El **miembro ab** de los identificadores de entrada creados por proveedores de libreta de direcciones y almacén de mensajes se compone de dos partes: una estructura [MAPIUID](mapiuid.md) de 16 bytes que identifica al proveedor de servicios y una parte para identificar el objeto. **MAPIUID** es una estructura que contiene un identificador único global o GUID. Un GUID es un identificador independiente del orden de bytes que se puede crear mediante la Microsoft Visual Studio *crear GUID**. 
  
Un proveedor de servicios registra su estructura **MAPIUID** con MAPI durante el proceso de inicio de sesión en una llamada al método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Cuando un cliente llama a un **método OpenEntry** para obtener acceso a un objeto, MAPI usa la estructura **MAPIUID** para determinar qué proveedor de servicios puede proporcionar ese acceso. Los proveedores de servicios deben usar la misma estructura **MAPIUID** para todas las versiones de su DLL. Esto permite a los clientes con la versión más reciente responder a los mensajes enviados y guardados con la versión anterior. 
  
El resto del **miembro ab** después de **MAPIUID** de 16 bytes contiene datos binarios específicos del proveedor de servicios para identificar objetos concretos. No hay un tamaño fijo para esta parte del identificador de entrada. Puede ser de cualquier tamaño, dentro de la razón. Normalmente, un proveedor de servicios incluye la siguiente información en esta parte de sus identificadores de entrada: 
  
- Información de versión: dado que es habitual que un proveedor de servicios cambie el formato de sus identificadores de entrada de una versión a otra, el almacenamiento de información de versión permite determinar rápidamente cómo descifrar cualquier identificador de entrada.
    
- Información de ubicación: la información de ubicación son datos que dan a un proveedor de servicios un indicador de cómo localizar el objeto representado por el identificador de entrada. Por ejemplo, un proveedor de servicios puede almacenar el desplazamiento del disco para el último lugar de un archivo de datos en el que se ha almacenado el objeto. Dado que este tipo de información puede cambiar con el tiempo, los proveedores de servicios deben proporcionar varias formas de localizar objetos en sus identificadores de entrada.
    
Aunque los proveedores de servicios pueden reciclar sus identificadores de entrada, deben evitar esta práctica. Si es necesario reutilizar un identificador de entrada, los proveedores de servicios deben hacer que el período de tiempo que transcurra entre el uso inicial y la reutilización el mayor tiempo posible. Además, el identificador de entrada debe reasignarse a otro objeto del mismo tipo. Es decir, un identificador de entrada determinado no debe asociarse primero con un mensaje y luego con una carpeta.
  
## <a name="see-also"></a>Vea también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

