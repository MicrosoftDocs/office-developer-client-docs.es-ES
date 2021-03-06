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
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415666"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera la posición actual de fila de tabla del cursor, basándose en un valor fraccional.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameters

 _lpulRow_
  
> [salida] Puntero al número de la fila actual. El número de fila está basado en cero; la primera fila de la tabla es cero. 
    
 _lpulNumerator_
  
> [salida] Puntero al numerador de la fracción que identifica la posición de la tabla.
    
 _lpulDenominator_
  
> [salida] Puntero al denominador de la fracción que identifica la posición de la tabla. El  _parámetro lpulDenominator_ no puede ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El método devuelve valores válidos  _en lpulRow_,  _lpulNumerator_ y  _lpulDenominator_.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::QueryPosition** determina la posición de fila actual y devuelve el número de la fila actual y un valor fraccionario que indica su posición relativa al final de la tabla. MAPI define la fila actual como la siguiente fila que se va a leer. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario devolver el número exacto de filas de la tabla para el parámetro  _lpulDenominator;_ puede ser una aproximación. 
  
Si no puede determinar la fila actual, devuelva un valor de 0xFFFFFFFF en  _lpulRow_.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **QueryPosition para** colocar un cuadro de desplazamiento en una barra de desplazamiento. Por ejemplo, en una tabla que contiene 100 filas, si **QueryPosition** devuelve un valor de 75 en el parámetro  _lpulNumerator,_ 100 en el parámetro  _lpulDenominator_ y 75 en el parámetro  _lpulRow,_ puede colocar el cuadro de desplazamiento 3/4 del camino a través de la barra de desplazamiento. 
  
No confíe en que el valor de  _lpulDenominator_ sea el número de filas de la tabla. **QueryPosition** no siempre puede identificar la fila exacta en la que se sitúa el cursor. 
  
Una llamada a **QueryPosition** puede implicar grandes cantidades de memoria, especialmente para tablas categorizadas grandes. Si el  _parámetro lpulRow_ se establece en 0xFFFFFFFF, se requería demasiada memoria para **que QueryPosition** determinara la fila actual. Llame al [método IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) para colocar la tabla en la fila identificada por los parámetros _lpulNumerator_ e _lpulDenominator._ Sin embargo, no siempre esperes **que SeekRowApprox** establezca como la posición actual la misma fila que **QueryPosition** tendría si la memoria no hubiera sido un factor. 
  
## <a name="see-also"></a>Vea también



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

