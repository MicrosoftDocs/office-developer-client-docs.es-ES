---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584341"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Recupera la posición de fila de tabla actual del cursor, basándose en un valor decimal.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parámetros

 _lpulRow_
  
> [out] Puntero al número de la fila actual. El número de fila es de base cero; la primera fila en la tabla es cero. 
    
 _lpulNumerator_
  
> [out] Puntero al numerador de la fracción que identifica la posición de la tabla.
    
 _lpulDenominator_
  
> [out] Puntero al denominador de la fracción que identifica la posición de la tabla. El parámetro _lpulDenominator_ no puede ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El método devuelve los valores válidos en _lpulRow_, _lpulNumerator_y _lpulDenominator_.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::QueryPosition** determina la posición de la fila actual y devuelve el número de la fila actual y un valor decimal que indica su posición relativa al final de la tabla. MAPI define la fila actual como la siguiente fila se leerá. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No es necesario devolver el número exacto de filas en la tabla para el parámetro _lpulDenominator_ ; puede ser una aproximación. 
  
Si no puede determinar la fila actual, devolverá un valor de 0xFFFFFFFF en _lpulRow_.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **QueryPosition** para colocar un cuadro de desplazamiento en una barra de desplazamiento. Por ejemplo, en una tabla que contiene 100 filas, si **QueryPosition** devuelve un valor de 75 en el parámetro _lpulNumerator_ , 100 en el parámetro _lpulDenominator_ y 75 en el parámetro _lpulRow_ , se puede colocar el cuadro de desplazamiento 3/4 de la forma a través de la barra de desplazamiento. 
  
No confíe en el valor de _lpulDenominator_ es el número de filas de la tabla. **QueryPosition** no siempre puede identificar la fila exacta que se coloca el cursor en. 
  
Una llamada a **QueryPosition** podría implicar grandes cantidades de memoria, especialmente para grandes tablas ordenadas por categorías. Si el parámetro _lpulRow_ se establece en 0xFFFFFFFF, demasiada memoria era necesaria para **QueryPosition** determinar la fila actual. Llame al método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) para colocar la tabla a la fila identificada por los parámetros _lpulNumerator_ y _lpulDenominator_ . Sin embargo, no siempre se puede esperar **SeekRowApprox** para establecer que la posición actual de la misma fila **que QueryPosition** tendría si memoria si no se hubiese un factor. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

