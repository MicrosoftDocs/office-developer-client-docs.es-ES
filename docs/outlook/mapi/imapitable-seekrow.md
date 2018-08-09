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
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817602"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**Hace referencia a**: Outlook 
  
Mueve el cursor a una posición específica en la tabla.
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>Parámetros

 _bkOrigin_
  
> [entrada] El marcador que identifica la posición inicial de la operación de búsqueda. Un marcador se puede crear mediante el método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) , o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Inicia la operación de búsqueda desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Inicia la operación de búsqueda de la fila en la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Inicia la operación de búsqueda desde el final de la tabla. 
    
 _lRowCount_
  
> [entrada] El recuento con signo del número de filas para mover, empezando por el marcador identificado mediante el parámetro _bkOrigin_ . 
    
 _lplRowsSought_
  
> [out] Si _lRowCount_ es un puntero válido en los puntos de entrada, _lplRowsSought_ para el número de filas que se han procesado en la operación de búsqueda, el inicio de sesión de los cuales indica la dirección de búsqueda, hacia delante o hacia atrás. Si _lRowCount_ es negativo, _lplRowsSought_ es negativo. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación seek fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de búsqueda de fila de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador especificado en el parámetro _bkOrigin_ no es válido porque se quitó o porque es más allá de la última fila solicitada. 
    
MAPI_W_POSITION_CHANGED 
  
> La llamada se ha realizado correctamente, pero ya no se establece el marcador especificado en el parámetro _bkOrigin_ en la misma fila como estaba cuando se usó por última vez. Si no se ha usado el marcador, ya no es en la misma posición que tenía cuando se creó. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::SeekRow** establece una nueva posición de BOOKMARK_CURRENT para el cursor. El parámetro _lRowCount_ indica el número de filas que se mueve el cursor y la dirección del movimiento. 
  
Si la posición resultante es más allá de la última fila de la tabla, se coloca el cursor después de la última fila. Si la posición resultante es antes de la primera fila de la tabla, se coloca el cursor al principio de la primera fila. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si la fila que apunta _bkOrigin_ ya no existe en la tabla y no se puede establecer una nueva posición para el marcador, devolver MAPI_E_INVALID_BOOKMARK. Si la fila que apunta _bkOrigin_ ya no existe y se puede establecer una nueva posición para el marcador, devolver MAPI_W_POSITION_CHANGED. 
  
Aún se puede usar un marcador que señala a una fila que se contrae fuera de la vista de tabla. Si el autor de la llamada intenta mover el cursor a como un marcador, mueva el cursor a la siguiente fila visible y devolver MAPI_W_POSITION_CHANGED. 
  
Puede mover los marcadores para posiciones contraídos fuera de la vista, en el momento de uso o en el momento en que se contrae la fila. Si se mueve un marcador en el momento en que la fila está contraída, tenga un poco en el marcador que indica si el marcador ha movido desde su última utilización o, si no tiene nunca se ha usado, desde su creación.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para indicar un movimiento con versiones anteriores para **SeekRow**, pase un valor negativo en _lRowCount_. Para buscar hasta el principio de la tabla, pase cero en _lRowCount_ y el valor BOOKMARK_BEGINNING en _bkOrigin_. 
  
Si hay una gran cantidad de filas de la tabla, la operación **SeekRow** puede ser lenta. Rendimiento también puede verse afectado si requieren un recuento de filas que se devolverán en el contenido del parámetro _lplRowsSought_ . 
  
 **SeekRow** devuelve el número de filas realmente buscado a través de, positivo o negativo, en la variable que apunta _lRowCount_. En funcionamiento normal, debe devolver el mismo valor para _lplRowsSought_ que se pasa para _lRowCount_, a menos que la búsqueda alcanzado el principio o al final de la tabla. 
  
No establezca _lRowCount_ a un número mayor que 50. Para buscar a través de un número mayor de filas, utilice el método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::ProcessMailboxTable  <br/> |MFCMAPI, utiliza el método **IMAPITable::SeekRow** para encontrar el principio de la tabla antes del procesamiento.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

