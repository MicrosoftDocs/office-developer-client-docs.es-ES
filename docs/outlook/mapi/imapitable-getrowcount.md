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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425606"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el número total de filas de la tabla. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Reserve debe ser cero.
    
 _lpulCount_
  
> contempla Puntero al número de filas de la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El recuento de filas se devolvió correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de recuperación de recuento de filas. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no puede calcular el número de filas.
    
MAPI_W_APPROX_COUNT 
  
> La llamada se realizó correctamente, pero se devolvió un recuento de filas aproximado porque no se pudo determinar el recuento de filas exacto, posiblemente debido a restricciones de memoria. Para probar esta advertencia, use la macro **HR_FAILED** . Consulte [uso de macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: GetRowCount** recupera el número total de filas de una tabla. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si no puede determinar el número exacto de filas de la tabla, devuelva MAPI_W_APPROX_COUNT y un recuento de filas aproximado en el contenido del parámetro _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Use **GetRowCount** para averiguar el número de filas que contiene una tabla antes de realizar una llamada al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar los datos. Si hay menos de veinte filas en la tabla, es seguro llamar a **QueryPosition** para recuperar toda la tabla. Si hay más de veinte filas en la tabla, considere la posibilidad de realizar varias llamadas a **QueryPosition** y limitar el número de filas recuperadas en cada llamada. 
  
Algunas tablas no admiten **GetRowCount** y devuelven MAPI_E_NO_SUPPORT. Si no se admite **GetRowCount** , una alternativa podría ser llamar al [IMAPITable:: QueryPosition](imapitable-queryposition.md). Con los resultados de **QueryPosition**, puede determinar la relación entre la fila actual y la última fila. 
  
Cuando **GetRowCount** devuelve MAPI_E_BUSY porque temporalmente no puede recuperar un recuento de filas, llame al método [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) . Cuando **WaitForCompletion** devuelva, vuelva a intentar la llamada a **GetRowCount**. Otra forma de detectar si una operación asincrónica está en curso es llamar al método [IMAPITable:: getStatus](imapitable-getstatus.md) y comprobar el contenido del parámetro _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI usa el método **IMAPITable:: GetRowCount** para determinar cuántas filas hay en la tabla de origen, por lo que se puede asignar memoria para realizar la copia.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

