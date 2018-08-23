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
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579721"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llama a una función interna para comprobar si que las aplicaciones cliente de los parámetros han pasado a proveedores de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parámetros

 _eMethod_
  
> [entrada] Especifica el (enumeración), el método para validar. 
    
 _Primero_
  
> [entrada] Puntero al primer argumento en la pila.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Todos los parámetros son válidos. 
    
MAPI_E_CALL_FAILED 
  
> Uno o varios de los parámetros no son válidos.
    
## <a name="remarks"></a>Comentarios

Parámetros pasados entre MAPI y servicio proveedores se supone que sea correcta y se sincronizan sólo depuración validación con la macro [CheckParms](checkparms.md) . Proveedores deben comprobar todos los parámetros que se pasó por las aplicaciones cliente, pero los clientes deben se presupone que MAPI y proveedor de parámetros correctos. Use la macro **HR_FAILED** para comprobar los valores devueltos. 
  
 **ValidateParms** se llama de manera diferente dependiendo de si el código de llamada es C o C++. C++ pasa un parámetro implícito conocido como _este_ para cada llamada al método, que se convierte en explícitas en C y es la dirección del objeto. El primer parámetro, _eMethod_, es un enumerador realizado desde la interfaz y el método que se está validando e indica los parámetros que se espera encontrar en la pila. El segundo parámetro es diferente para C y C++. En C++ se denomina _primer_, y es el primer parámetro para el método que se está validando. El segundo parámetro para el lenguaje C, _ppThis_, es la dirección del primer parámetro para el método que es siempre un puntero de objeto. En ambos casos, el segundo parámetro proporciona la dirección del principio de la lista de parámetros del método y en función de _eMethod_, mueve hacia abajo de la pila y valida los parámetros. 
  
Los proveedores que implementan las interfaces comunes, como **IMAPITable** y **IMAPIProp** siempre deben comprobar los parámetros mediante la función **ValidateParms** con el fin de realizar seguro de coherencia entre todos los proveedores. Se han definido las funciones de validación del parámetro adicional para que algunos tipos de parámetro complejo que se usará en su lugar, según corresponda. Vea los temas de referencia para las funciones siguientes: 
  
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
    
Métodos heredados usan la misma validación de parámetros como la interfaz de la que heredan. Por ejemplo, la comprobación de parámetros de **IMessage** y **IMAPIProp** deben ser el mismo. 
  
## <a name="see-also"></a>Recursos adicionales



[UlValidateParms](ulvalidateparms.md)

