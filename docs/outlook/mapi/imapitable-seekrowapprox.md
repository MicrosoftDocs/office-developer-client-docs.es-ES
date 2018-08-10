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
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817617"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Hace referencia a**: Outlook 
  
Mueve el cursor a una posición aproximada fraccionaria en la tabla. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parámetros

 _ulNumerator_
  
> [entrada] Puntero a la numerador de la fracción que representa la posición de la tabla. Si el parámetro _ulNumerator_ es cero, se coloca el cursor al principio de la tabla independientemente del valor de denominador. Si _ulNumerator_ es igual que el parámetro _ulDenominator_ , se coloca el cursor después de la última fila de tabla. 
    
 _ulDenominator_
  
> [entrada] Puntero a como denominador de la fracción que representa la posición de la tabla. El parámetro _ulDenominator_ no puede ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación seek fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la fila que busquen la operación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
## <a name="remarks"></a>Comentarios

La posición del cursor en una tabla después de una llamada al método **IMAPITable:: SeekRowApprox** es la fracción de forma heurística y puede no ser exacta. Por ejemplo, ciertos proveedores podrían implementar una tabla en la parte superior un árbol binario, tratando punto intermedio de la tabla como la parte superior del árbol por motivos de rendimiento. Si no se equilibra el árbol, a continuación, el punto medio utilizado podría no ser exactamente la mitad a través de la tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **SeekRowApprox** para proporcionar los datos para una implementación de la barra de desplazamiento. Por ejemplo, si el usuario coloca el cuadro de desplazamiento 2/3 hacia abajo de la barra de desplazamiento, se puede modelar esa acción llamando a **SeekRowApprox** y pasando un valor fraccionario equivalente mediante _ulNumerator_ y _ulDenominator_. La búsqueda de **SeekRowApprox** siempre es absoluta desde el principio de la tabla. Para desplazarse hasta el final de la tabla, los valores de _ulNumerator_ y _ulDenominator_ deben ser el mismo. 
  
Usar cualquier combinación de número es adecuado. Es decir, para buscar a una posición intermedia a través de la tabla, puede especificar 1/2, 10/20 o 50/100. 
  
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)

