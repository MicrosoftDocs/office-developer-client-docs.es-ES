---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436811"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para comprobar los parámetros que las aplicaciones cliente han pasado a los proveedores de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> [in] Especifica, por enumeración, el método que se debe validar. 
    
 _Primero_
  
> [in] Puntero al primer argumento de la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Todos los parámetros son válidos. 
    
MAPI_E_CALL_FAILED 
  
> Uno o varios de los parámetros no son válidos.
    
## <a name="remarks"></a>Comentarios

Se supone que los parámetros pasados entre MAPI y los proveedores de servicios son correctos y solo se someten a validación de depuración con la macro [CheckParms.](checkparms.md) Los proveedores deben comprobar todos los parámetros pasados por las aplicaciones cliente, pero los clientes deben asumir que los parámetros MAPI y del proveedor son correctos. Use la **macro HR_FAILED** para probar los valores devueltos. 
  
 **ValidateParms** se llama de forma diferente en función de si el código de llamada es C o C++. C++ pasa un parámetro implícito conocido como esto  _a_ cada llamada de método, que se convierte en explícita en C y es la dirección del objeto. El primer parámetro,  _eMethod_, es un enumerador hecho a partir de la interfaz y el método que se va a validar y indica qué parámetros esperar encontrar en la pila. El segundo parámetro es diferente para C y C++. En C++ se denomina  _First_ y es el primer parámetro del método que se va a validar. El segundo parámetro para el lenguaje C,  _ppThis_, es la dirección del primer parámetro para el método que siempre es un puntero de objeto. En ambos casos, el segundo parámetro proporciona la dirección del principio de la lista de parámetros del método y, según  _eMethod,_ baja la pila y valida los parámetros. 
  
Los proveedores que implementan interfaces comunes como **IMAPITable** e **IMAPIProp** siempre deben comprobar los parámetros mediante la **función ValidateParms** para garantizar la coherencia entre todos los proveedores. Se han definido funciones de validación de parámetros adicionales para algunos tipos de parámetros complejos que se usarán según corresponda. Vea los temas de referencia para las siguientes funciones: 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Los métodos heredados usan la misma validación de parámetros que la interfaz de la que heredan. Por ejemplo, la comprobación de parámetros **para IMessage** e **IMAPIProp** debe ser la misma. 
  
## <a name="see-also"></a>Vea también



[UlValidateParms](ulvalidateparms.md)

