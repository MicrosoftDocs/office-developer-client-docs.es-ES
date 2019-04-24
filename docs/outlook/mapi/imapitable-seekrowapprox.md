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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328843"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mueve el cursor a una posición fraccional aproximada en la tabla. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameters

 _ulNumerator_
  
> a Puntero al numerador de la fracción que representa la posición de la tabla. Si el parámetro _ulNumerator_ es cero, el cursor se coloca al principio de la tabla independientemente del valor del denominador. Si _ulNumerator_ es igual al parámetro _ulDenominator_ , el cursor se coloca detrás de la última fila de la tabla. 
    
 _ulDenominator_
  
> a Puntero al denominador de la fracción que representa la posición de la tabla. El parámetro _ulDenominator_ no puede ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se realizó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que evita que la operación de búsqueda de filas se inicie. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
## <a name="remarks"></a>Comentarios

La posición del cursor en una tabla después de una llamada al método **IMAPITable:: SeekRowApprox** es heurísticamente la fracción y podría no ser exacta. Por ejemplo, algunos proveedores pueden implementar una tabla sobre un árbol binario, tratando la mitad central de la tabla como la parte superior del árbol por motivos de rendimiento. Si no se equilibra el árbol, es posible que el punto medio utilizado no sea exactamente la mitad de la tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a **SeekRowApprox** para proporcionar los datos para la implementación de una barra de desplazamiento. Por ejemplo, si el usuario coloca el cuadro de desplazamiento 2/3 hacia abajo en la barra de desplazamiento, puede modelar esa acción llamando a **SeekRowApprox** y pasando un valor fraccionario equivalente mediante _ulNumerator_ y _ulDenominator_. La búsqueda de **SeekRowApprox** siempre es absoluta desde el principio de la tabla. Para ir al final de la tabla, los valores de _ulNumerator_ y _ulDenominator_ deben ser iguales. 
  
Use cualquier esquema de números adecuado. Es decir, para buscar una posición a mitad de la tabla, puede especificar 1/2, 10/20 o 50/100. 
  
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)

