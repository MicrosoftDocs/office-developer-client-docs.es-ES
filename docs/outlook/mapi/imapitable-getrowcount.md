---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a591a49c1cb0ec936d09d59b4632d15e4842dd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817599"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Se aplica a**: Outlook 
  
Devuelve el número total de filas en la tabla. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lpulCount_
  
> [out] Puntero al número de filas de la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El recuento de filas se devolvió correctamente.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de recuperación del recuento de fila de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no puede calcular el número de filas.
    
MAPI_W_APPROX_COUNT 
  
> La llamada se ha realizado correctamente, pero se devolvió un recuento de filas aproximado debido a que el número exacto de filas no se puede determinar, posiblemente, debido a las restricciones de memoria. Para probar esta advertencia, utilice la macro **HR_FAILED** . Vea [uso de Macros para el tratamiento de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Notas

El método **IMAPITable::GetRowCount** recupera el número total de filas en una tabla. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si no puede determinar el número de fila exacto de la tabla, MAPI_W_APPROX_COUNT devuelto y una fila aproximada contar en el contenido del parámetro _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Uso **GetRowCount** para averiguar el número de filas de una tabla contiene antes de realizar una llamada al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos. Si hay menos de veinte filas en la tabla, es seguro llamar **QueryPosition** para recuperar toda la tabla. Si hay más de veinte filas de la tabla, considere la posibilidad de realizar varias llamadas a **QueryPosition** y limitar el número de filas recuperadas en cada llamada. 
  
Algunas tablas no admiten **GetRowCount** y devolver MAPI_E_NO_SUPPORT. Si no se admite **GetRowCount** , es posible una alternativa llamar a [IMAPITable::QueryPosition](imapitable-queryposition.md). Con los resultados de **QueryPosition**, puede determinar la relación entre la fila actual y la última fila. 
  
Cuando **GetRowCount** devuelve MAPI_E_BUSY porque está temporalmente no se puede recuperar un recuento de filas, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) . Cuando se devuelve **WaitForCompletion** , vuelva a intentar la llamada a **GetRowCount**. Llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) y compruebe el contenido del parámetro _lpulTableState_ es otra forma de detectar si una operación asincrónica está en curso. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI usa el método **IMAPITable::GetRowCount** para determinar cuántas filas se encuentran en la tabla de origen por lo que se puede asignar memoria para realizar la copia.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable:: QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

