---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435183"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre un problema de procesamiento de propiedades o atributos que se produjo durante la codificación o decodificación de una secuencia de formato de encapsulamiento neutro de transporte (TNEF).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Miembros

 **ulComponent**
  
> Tipo de procesamiento durante el cual se produjo el problema. Si el problema se produjo durante el procesamiento de mensajes, el **miembro ulComponent** se establece en cero. Si el problema se produjo durante el procesamiento de datos adjuntos, **ulComponent** se establece igual al valor de PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) correspondiente.
    
 **ulAttribute**
  
> Atributo asociado a la propiedad indicada por el miembro **ulPropTag** o, cuando se produce el problema de procesamiento TNEF al decodificar un bloque de encapsulación, uno de los siguientes valores: 
    
 _attMAPIProps_
  
> Nivel de mensaje
    
 _attAttachment_
  
> Nivel de datos adjuntos
    
 **ulPropTag**
  
> Etiqueta de propiedad de la propiedad que provocó el problema de procesamiento TNEF, excepto cuando el problema se produce al decodificar un bloque de encapsulación, en cuyo caso **ulPropTag** se establece en cero. 
    
 **scode**
  
> Valor de error que indica el problema detectado durante el procesamiento.
    
## <a name="remarks"></a>Comentarios

Si no se genera una estructura **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación puede continuar con la suposición de que el procesamiento de ese atributo o propiedad se ha hecho correctamente. La única excepción se produce cuando el problema se produjo durante la decodificación de un bloque de encapsulación. En este caso, la decodificación del componente correspondiente al bloque se detiene y la decodificación continúa en otro componente. 
  
## <a name="see-also"></a>Consulte también



[STnefProblemArray](stnefproblemarray.md)
  
[Propiedad canónica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

