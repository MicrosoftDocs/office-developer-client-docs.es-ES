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
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592062"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una propiedad con nombre que se utiliza con un formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
   
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

## <a name="members"></a>Members

 **ulFlags**
  
> Marcas que se usan para distinguir el formato de las cadenas de la estructura de **SMAPIFormProp** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece MAPI_UNICODE., las cadenas están en formato ANSI.
    
 **nPropType**
  
> Tipo de la propiedad con nombre, con la palabra más importante que se establece en cero. 
    
 **nmid**
  
> Nombre de la propiedad con nombre, que incluye una estructura **GUID** que identifica el valor de propiedad set y una numérica o de cadena que representa un nombre de identificador y el formulario de interfaz. 
    
 **pszDisplayName**
  
> Puntero en el nombre para mostrar de la propiedad con nombre.
    
 **nSpecialType**
  
> Valor que describe el tipo de datos incluidos en el miembro **u** . Los valores posibles son los siguientes: 
    
FPST_VANILLA 
  
> El miembro **u** no contiene una enumeración. 
    
FPST_ENUM_PROP 
  
> El miembro **u** contiene una estructura que describe una enumeración. 
    
 **s**
  
> Unión que describe la asociación entre el nombre y el número de la propiedad con nombre. Mediante el uso de algunas propiedades, el miembro **u** está vacío. Con otras propiedades, se representa en una estructura que consta de los siguientes miembros: 
    
 **nmidIdx**
  
> La estructura [MAPINAMEID](mapinameid.md) que contiene el conjunto de propiedades y el identificador de la propiedad con nombre. 
    
 **cfpevAvailable**
  
> Recuento de las estructuras de [SMAPIFormPropEnumVal](smapiformpropenumval.md) en la matriz indicada por el miembro **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Puntero a una matriz de estructuras **SMAPIFormPropEnumVal** , cada uno de los cuales contiene un valor para la propiedad con nombre. 
    
## <a name="remarks"></a>Comentarios

La estructura **SMAPIFormProp** contiene información sobre una propiedad de formulario que se usa como parte de las definiciones de la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) . **nSpecialType** contiene una etiqueta que se aplica a la unión **u** que forma parte de **SMAPIFormProp**.
  
## <a name="see-also"></a>Recursos adicionales



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Estructuras MAPI](mapi-structures.md)

