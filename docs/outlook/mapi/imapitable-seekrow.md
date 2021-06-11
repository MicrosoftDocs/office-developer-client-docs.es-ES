---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413048"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mueve el cursor a una posición específica de la tabla.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Parameters

 _bkOrigin_
  
> [in] Marcador que identifica la posición inicial de la operación de búsqueda. Se puede crear un marcador mediante el método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Inicia la operación de búsqueda desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Inicia la operación de búsqueda desde la fila de la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Inicia la operación de búsqueda desde el final de la tabla. 
    
 _lRowCount_
  
> [in] Recuento firmado del número de filas que se moverá, empezando por el marcador identificado por el _parámetro bkOrigin._ 
    
 _lplRowsSought_
  
> [salida] Si  _lRowCount_ es un puntero válido en la entrada,  _lplRowsSought_ apunta al número de filas que se procesaron en la operación seek, cuyo signo indica la dirección de la búsqueda, hacia delante o hacia atrás. Si  _lRowCount_ es negativo,  _lplRowsSought_ es negativo. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de búsqueda de filas. Debe permitirse completar la operación en curso o detenerse.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador especificado en el  _parámetro bkOrigin_ no es válido porque se quitó o porque está más allá de la última fila solicitada. 
    
MAPI_W_POSITION_CHANGED 
  
> La llamada se ha hecho correctamente, pero el marcador especificado en el parámetro  _bkOrigin_ ya no se establece en la misma fila que cuando se usó por última vez. Si no se ha usado el marcador, ya no está en la misma posición que cuando se creó. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::SeekRow** establece una nueva BOOKMARK_CURRENT posición del cursor. El  _parámetro lRowCount_ indica el número de filas que mueve el cursor y la dirección del movimiento. 
  
Si la posición resultante está más allá de la última fila de la tabla, el cursor se coloca después de la última fila. Si la posición resultante es anterior a la primera fila de la tabla, el cursor se coloca al principio de la primera fila. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si la fila señalada por  _bkOrigin_ ya no existe en la tabla y no se puede establecer una nueva posición para el marcador, MAPI_E_INVALID_BOOKMARK. Si la fila señalada por  _bkOrigin_ ya no existe y puede establecer una nueva posición para el marcador, devuelva MAPI_W_POSITION_CHANGED. 
  
Todavía se puede usar un marcador que apunte a una fila que se contrae fuera de la vista de tabla. Si el autor de la llamada intenta mover el cursor a dicho marcador, mueva el cursor a la siguiente fila visible y vuelva a MAPI_W_POSITION_CHANGED. 
  
Puede mover marcadores para las posiciones contraidas fuera de la vista, ya sea en el momento de su uso o en el momento en que se contrae la fila. Si se mueve un marcador en el momento en que se contrae la fila, mantenga un poco en el marcador que indica si el marcador se ha movido desde su último uso o, si nunca se ha usado, desde su creación.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para indicar un movimiento hacia atrás **para SeekRow**, pase un valor negativo en  _lRowCount_. Para buscar al principio de la tabla, pase cero en  _lRowCount_ y el valor BOOKMARK_BEGINNING  _en bkOrigin_. 
  
Si hay muchas filas en la tabla, la **operación SeekRow** puede ser lenta. El rendimiento también puede verse afectado si necesita que se devuelva un recuento de filas en el contenido del parámetro _lplRowsSought._ 
  
 **SeekRow** devuelve el número de filas realmente buscadas, positivas o negativas, en la variable apuntada por  _lRowCount_. En operación normal, debe devolver el mismo valor para  _lplRowsSought_ que se pasó para  _lRowCount_, a menos que la búsqueda alcanzara el principio o el final de la tabla. 
  
No establezca  _lRowCount en_ un número mayor que 50. Para buscar a través de un número mayor de filas, use el [método IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI usa el **método IMAPITable::SeekRow** para buscar el principio de la tabla antes del procesamiento.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

