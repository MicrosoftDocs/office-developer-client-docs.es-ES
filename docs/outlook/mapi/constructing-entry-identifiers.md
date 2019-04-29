---
title: Crear identificadores de entrada
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
# <a name="constructing-entry-identifiers"></a>Crear identificadores de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los identificadores de entrada se construyen con la estructura [EntryID](entryid.md) . La estructura **EntryID** está compuesta por una marca que describe los atributos del identificador de entrada y el identificador de entrada real. 
  
## <a name="entryid-structure"></a>Estructura ENTRYID

La estructura **EntryID** se define de la siguiente manera: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM es una constante que se define en el archivo de encabezado MapiDefs. h. 
  
El primer byte del miembro **abFlags** de 4 bytes describe el tipo y uso del identificador de entrada y puede tener los valores siguientes: 
  
- MAPI_NOTRECI: indica que el identificador de entrada no se puede usar como un destinatario en un mensaje.
    
- MAPI_NOTRESERVED: indica que otros usuarios no pueden tener acceso al identificador de entrada.
    
- MAPI_NOW: indica que el identificador de entrada no se puede usar en otros momentos.
    
- MAPI_SHORTTERM: indica que el identificador de entrada es a corto plazo. Se deben establecer todos los demás valores de este byte, a menos que se permitan otros usos del identificador de entrada.
    
- MAPI_THISSESSION: indica que el identificador de entrada no se puede usar en otras sesiones.
    
- MAPI_NOTRESERVED: indica que otros proveedores de servicios pueden usar el identificador de entrada para otros objetos.
    
El miembro **AB** de los identificadores de entrada que crea la libreta de direcciones y los proveedores de almacenamiento de mensajes consta de dos partes: una estructura [MAPIUID](mapiuid.md) de 16 bytes que identifica al proveedor de servicios y una parte para identificar el objeto. **MAPIUID** es una estructura que contiene un identificador único global (GUID). Un GUID es un identificador independiente de orden de bytes que se puede crear mediante la herramienta Microsoft Visual Studio*Create GUID**. 
  
Un proveedor de servicios registra su estructura **MAPIUID** con MAPI durante el proceso de inicio de sesión en una llamada al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) . Cuando un cliente llama a un método **OpenEntry** para tener acceso a un objeto, MAPI usa la estructura **MAPIUID** para determinar qué proveedor de servicios puede proporcionar ese acceso. Los proveedores de servicios deben usar la misma estructura **MAPIUID** para todas las versiones de su dll. Esto permite que los clientes con la versión más reciente respondan a los mensajes enviados y guardados con la versión anterior. 
  
El resto del miembro **AB** después del **MAPIUID** de 16 bytes contiene datos binarios específicos del proveedor de servicios para identificar objetos determinados. No hay ningún tamaño fijo para esta parte del identificador de entrada. Puede tener cualquier tamaño, en razón. Un proveedor de servicios suele incluir la siguiente información en esta parte de sus identificadores de entrada: 
  
- Información de la versión: debido a que es habitual que un proveedor de servicios cambie el formato de sus identificadores de entrada de una versión a otra, el almacenamiento de la información de versión permite determinar rápidamente cómo descifrar cualquier identificador de entrada.
    
- Información de Ubicación: la información de ubicación es un dato que proporciona a un proveedor de servicios un indicador de cómo localizar el objeto representado por el identificador de entrada. Por ejemplo, un proveedor de servicios puede almacenar el desplazamiento de disco para la última posición en un archivo de datos que se almacenó el objeto. Debido a que este tipo de información puede cambiar con el tiempo, los proveedores de servicios deben proporcionar varias formas de localizar los objetos en sus identificadores de entrada.
    
Aunque los proveedores de servicios pueden reciclar sus identificadores de entrada, deben evitar este procedimiento. Si es necesario reutilizar un identificador de entrada, los proveedores de servicios deben realizar el período de tiempo que transcurre entre el uso inicial y la reutilización siempre que sea posible. Además, el identificador de entrada debe reasignarse a otro objeto del mismo tipo. Es decir, un identificador de entrada determinado no debe asociarse primero con un mensaje y luego con una carpeta.
  
## <a name="see-also"></a>Ver también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

