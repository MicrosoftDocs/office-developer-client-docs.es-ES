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
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816561"
---
# <a name="constructing-entry-identifiers"></a>Crear identificadores de entrada

  
  
**Hace referencia a**: Outlook 
  
Los identificadores de entrada se construyen con la estructura de la [propiedad ENTRYID](entryid.md) . La estructura de la **propiedad ENTRYID** consta de una marca que se describe los atributos del identificador de entrada y el identificador de entrada real. 
  
## <a name="entryid-structure"></a>Estructura de la propiedad ENTRYID

La estructura de la **propiedad ENTRYID** se define como sigue: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM es una constante que se define en el archivo de encabezado MapiDefs.h. 
  
El primer byte del miembro **abFlags** de 4 bytes describe el tipo y el uso del identificador de entrada y puede tener los valores siguientes: 
  
- MAPI_NOTRECI: Indica el identificador de entrada no se puede usar como un destinatario de un mensaje.
    
- MAPI_NOTRESERVED: Indica que otros usuarios no pueden obtener acceso el identificador de entrada.
    
- MAPI_NOW: Indica que el identificador de entrada no se puede usar en otros momentos.
    
- MAPI_SHORTTERM: Indica que el identificador de entrada es a corto plazo. Todos los otros valores de este byte deben estar establecidos a menos que se permiten otros usos del identificador de entrada.
    
- MAPI_THISSESSION: Indica que el identificador de entrada no se puede usar en otras sesiones.
    
- MAPI_NOTRESERVED: Indica que se puede usar el identificador de entrada por otros proveedores de servicios para otros objetos.
    
El miembro **ab** de los identificadores de entrada que se crea mediante proveedores de almacén de libreta de direcciones y el mensaje de dirección se compone de dos partes: una estructura [MAPIUID](mapiuid.md) de 16 bytes que identifica el proveedor de servicios y un dato para identificar el objeto. **MAPIUID** es una estructura que contiene un identificador único global o GUID. Un GUID es un identificador independiente del orden de bytes que se puede crear mediante el uso de Microsoft Visual Studio*Crear GUID** herramienta. 
  
Un proveedor de servicios registra su estructura **MAPIUID** con MAPI durante el proceso de inicio de sesión en una llamada al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) . Cuando un cliente llama a un método **OpenEntry** para tener acceso a un objeto, MAPI utiliza la estructura **MAPIUID** para determinar qué servicio proveedor puede proporcionar que tienen acceso. Proveedores de servicio deben usar la misma estructura **MAPIUID** para todas las versiones de su DLL. Esto permite a los clientes con la versión más reciente responder a los mensajes que se envían y se guardan con la versión más antigua. 
  
El resto del miembro **ab** después de la **MAPIUID** de 16 bytes contiene datos binarios de específico del proveedor de servicio para la identificación de determinados objetos. No hay ningún tamaño fijo para esta parte del identificador de entrada. Puede tener cualquier tamaño, dentro de motivo. Normalmente, un proveedor de servicios incluye la siguiente información en esta parte de sus identificadores de entrada: 
  
- Información de versión, dado que es común para un proveedor de servicios cambiar el formato de sus identificadores de entrada de una versión a otra, almacenar la información de versión hace posible determinar rápidamente cómo descifrar cualquier identificador de entrada.
    
- Información de ubicación: información de ubicación es datos que proporciona un indicador de cómo localizar el objeto representado por el identificador de entrada a un proveedor de servicios. Por ejemplo, un proveedor de servicios puede almacenar el disco de desplazamiento para el último lugar en un archivo de datos que se almacena el objeto. Debido a que este tipo de información puede cambiar con el tiempo, los proveedores de servicios deben proporcionar varias maneras para localizar objetos en sus identificadores de entrada.
    
Aunque los proveedores de servicios pueden reciclar sus identificadores de entrada, debe evitar esta práctica. Si es necesario volver a usar un identificador de entrada, los proveedores de servicios deben realizar el período de tiempo que debe transcurrir entre el uso inicial y la reutilización siempre que sea posible. Además, el identificador de entrada se debe reasignar a otro objeto del mismo tipo. Es decir, un identificador de entrada determinado no debe ser asociado en primer lugar con un mensaje y, a continuación, con una carpeta.
  
## <a name="see-also"></a>Vea también



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

