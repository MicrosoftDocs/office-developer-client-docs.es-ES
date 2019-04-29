---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416702"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una propiedad con nombre utilizada con un formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>Miembros

 **ulFlags**
  
> Marcas utilizadas para distinguir el formato de las cadenas en la estructura **SMAPIFormProp** . Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece MAPI_UNICODE, las cadenas están en formato ANSI.
    
 **nPropType**
  
> Tipo de la propiedad con nombre, con la palabra más significativa establecida en cero. 
    
 **nmid**
  
> Nombre de la propiedad con nombre, que incluye una estructura **GUID** que identifica el conjunto de propiedades y un valor numérico o de cadena que representa un identificador de interfaz y un nombre de formulario. 
    
 **pszDisplayName**
  
> Puntero al nombre para mostrar de la propiedad con nombre.
    
 **nSpecialType**
  
> Valor que describe el tipo de datos incluidos en el miembro **u** . Los valores posibles son los siguientes: 
    
FPST_VANILLA 
  
> El miembro **u** no contiene una enumeración. 
    
FPST_ENUM_PROP 
  
> El miembro **u** contiene una estructura que describe una enumeración. 
    
 **s**
  
> Unión que describe la asociación entre el nombre y el número de la propiedad con nombre. Mediante el uso de algunas propiedades, el miembro **u** está vacío. Con otras propiedades, se representa en una estructura que consta de los siguientes miembros: 
    
 **nmidIdx**
  
> Estructura [MAPINAMEID](mapinameid.md) que contiene el conjunto de propiedades y el identificador de la propiedad con nombre. 
    
 **cfpevAvailable**
  
> Número de estructuras [SMAPIFormPropEnumVal](smapiformpropenumval.md) en la matriz señalada por el miembro **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Puntero a una matriz de estructuras **SMAPIFormPropEnumVal** , cada una de las cuales contiene un valor para la propiedad con nombre. 
    
## <a name="remarks"></a>Comentarios

La estructura **SMAPIFormProp** contiene información sobre una propiedad de formulario usada como parte de las definiciones de la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contiene una etiqueta que se aplica a la Unión **u** que forma parte de **SMAPIFormProp**.
  
## <a name="see-also"></a>Ver también



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Estructuras MAPI](mapi-structures.md)

