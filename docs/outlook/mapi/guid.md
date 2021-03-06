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
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421588"
---
# <a name="guid"></a>GUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un identificador único global (GUID). 
  
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
  
> Un valor de datos enteros largos sin signo.
    
 **Data2**
  
> Un valor de datos enteros cortos sin signo.
    
 **Data3**
  
> Un valor de datos enteros cortos sin signo.
    
 **Data4**
  
> Una matriz de caracteres sin signo.
    
## <a name="remarks"></a>Comentarios

 **Las** estructuras GUID se usan en MAPI de la siguiente manera: 
  
- En las [estructuras MAPIUID](mapiuid.md) que identifican de forma única los proveedores de servicios. 
    
- Para identificadores de interfaz.
    
- En el conjunto de propiedades se establecen nombres de propiedades con nombre. 
    
Los proveedores de libreta de direcciones y almacén de mensajes generan **una estructura GUID** que se usará en su estructura **MAPIUID.** Al pasar el **MAPIUID** resultante a [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), estos proveedores de servicios informan a MAPI de su identificador único.
  
Además, se usan en la implementación de la llamada a procedimiento remoto (RPC) de Microsoft y el lenguaje de descripción del objeto (ODL). Para obtener más información acerca de estos usos, vea  *la Guía* y la referencia del programador RPC de Microsoft , Referencia del programador *OLE*  y  *Inside OLE*, *Segunda edición*  . 
  
La **estructura GUID** se define en la Referencia del programador de  *Win32*  . Los valores específicos **de las estructuras GUID** que se usan dentro de MAPI se definen en el archivo de encabezado MAPI Mapiguid.h. 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)


[Estructuras MAPI](mapi-structures.md)

