---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577698"
---
# <a name="guid"></a>GUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se describe un identificador único global (GUID). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiguid.h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> Un valor entero largo sin signo de los datos.
    
 **Data2**
  
> Un valor entero corto sin signo de los datos.
    
 **Data3**
  
> Un valor entero corto sin signo de los datos.
    
 **Data4**
  
> Una matriz de caracteres sin firmar.
    
## <a name="remarks"></a>Comentarios

 Estructuras **GUID** se usan en MAPI, como se indica a continuación: 
  
- En las estructuras [MAPIUID](mapiuid.md) que identifican los proveedores de servicios. 
    
- Para los identificadores de interfaz.
    
- En la propiedad establece los nombres de propiedades con nombre. 
    
Almacén de mensajes y dirección de los proveedores de libreta generan una estructura **GUID** para usar en su estructura **MAPIUID** . Al pasar el resultante **MAPIUID** al [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), estos proveedores de servicios de informar a MAPI de su identificador único.
  
Además, se usan en la implementación de llamada a procedimiento remoto (RPC) y el lenguaje de descripción de objetos (ODL). Para obtener más información acerca de estos usos, vea la *Guía y la referencia del programador de Microsoft RPC*, *referencia del programador de OLE* y *Dentro de OLE*, *Segunda edición* . 
  
La estructura **GUID** se define en la *referencia del programador de Win32* . Los valores específicos para las estructuras **GUID** que se usan dentro de MAPI se definen en el archivo de encabezado Mapiguid.h MAPI. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIUID](mapiuid.md)


[Estructuras MAPI](mapi-structures.md)

