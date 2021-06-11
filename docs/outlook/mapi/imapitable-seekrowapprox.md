---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412152"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mueve el cursor a una posición fraccional aproximada de la tabla. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameters

 _ulNumerator_
  
> [in] Puntero al numerador de la fracción que representa la posición de la tabla. Si el  _parámetro ulNumerator_ es cero, el cursor se coloca al principio de la tabla independientemente del valor denominador. Si  _ulNumerator_ es igual al parámetro  _ulDenominator,_ el cursor se coloca después de la última fila de la tabla. 
    
 _ulDenominator_
  
> [in] Puntero al denominador de la fracción que representa la posición de la tabla. El  _parámetro ulDenominator_ no puede ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de búsqueda de filas. Debe permitirse completar la operación en curso o detenerse.
    
## <a name="remarks"></a>Comentarios

La posición del cursor en una tabla después de una llamada al método **IMAPITable::SeekRowApprox** es heurísticamente la fracción y puede que no sea exacta. Por ejemplo, algunos proveedores pueden implementar una tabla en la parte superior de un árbol binario, tratando el punto medio de la tabla como la parte superior del árbol por motivos de rendimiento. Si el árbol no está equilibrado, es posible que el punto medio usado no esté exactamente a mitad de la tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llama a **SeekRowApprox para** proporcionar los datos de una implementación de barra de desplazamiento. Por ejemplo, si el usuario coloca el cuadro de desplazamiento 2/3 hacia abajo en la barra de desplazamiento, puede modelar esa acción llamando a **SeekRowApprox** y pasando un valor fraccionado equivalente mediante  _ulNumerator_ y  _ulDenominator_. La **búsqueda SeekRowApprox** siempre es absoluta desde el principio de la tabla. Para desplazarse al final de la tabla, los valores de  _ulNumerator_ y  _ulDenominator_ deben ser los mismos. 
  
Use cualquier esquema de números que sea apropiado. Es decir, para buscar una posición a mitad de la tabla, puede especificar 1/2, 10/20 o 50/100. 
  
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)

