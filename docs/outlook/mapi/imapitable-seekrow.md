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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328829"
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
  
> a Marcador que identifica la posición inicial de la operación de búsqueda. Un marcador se puede crear con el método [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Inicia la operación de búsqueda desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Inicia la operación de búsqueda desde la fila de la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Inicia la operación de búsqueda a partir del final de la tabla. 
    
 _lRowCount_
  
> a Recuento con signo del número de filas que se va a mover, a partir del marcador identificado por el parámetro _bkOrigin_ . 
    
 _lplRowsSought_
  
> contempla Si _lRowCount_ es un puntero válido en la entrada, _lplRowsSought_ apunta al número de filas que se procesaron en la operación de búsqueda, cuyo signo indica la dirección de la búsqueda, hacia delante o hacia atrás. Si _lRowCount_ es negativo, _lplRowsSought_ es negativo. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se realizó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que evita que la operación de búsqueda de filas se inicie. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador especificado en el parámetro _bkOrigin_ no es válido porque se quitó o porque está más allá de la última fila solicitada. 
    
MAPI_W_POSITION_CHANGED 
  
> La llamada se realizó correctamente, pero el marcador especificado en el parámetro _bkOrigin_ ya no se establece en la misma fila que tenía cuando se usó por última vez. Si no se ha utilizado el marcador, deja de estar en la misma posición que cuando se creó. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: SeekRow** establece una nueva posición de BOOKMARK_CURRENT para el cursor. El parámetro _lRowCount_ indica el número de filas que se mueve el cursor, así como la dirección del movimiento. 
  
Si la posición resultante está más allá de la última fila de la tabla, el cursor se coloca detrás de la última fila. Si la posición resultante se encuentra antes de la primera fila de la tabla, el cursor se coloca al principio de la primera fila. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si la fila a la que apunta _bkOrigin_ ya no existe en la tabla y no puede establecer una nueva posición para el marcador, devuelva MAPI_E_INVALID_BOOKMARK. Si la fila a la que apunta _bkOrigin_ ya no existe y puede establecer una nueva posición para el marcador, devuelva MAPI_W_POSITION_CHANGED. 
  
Todavía se puede usar un marcador que apunte a una fila contraída de la vista de tabla. Si el autor de la llamada intenta mover el cursor a dicho marcador, mueva el cursor a la siguiente fila visible y devuelva MAPI_W_POSITION_CHANGED. 
  
Puede mover los marcadores de los puestos contraídos fuera de la vista, ya sea en el momento de su uso o en el momento en que se contrae la fila. Si un marcador se mueve en el momento en que se contrae la fila, mantenga un bit en el marcador que indique si el marcador se ha movido desde el último uso o, si nunca se ha usado, desde su creación.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para indicar un movimiento hacia atrás para **SeekRow**, pase un valor negativo en _lRowCount_. Para buscar el principio de la tabla, pase cero en _lRowCount_ y el valor BOOKMARK_BEGINNING en _bkOrigin_. 
  
Si hay muchas filas en la tabla, la operación **SeekRow** puede ser lenta. El rendimiento también puede verse afectado si requiere que se devuelva un recuento de filas en el contenido del parámetro _lplRowsSought_ . 
  
 **SeekRow** devuelve el número de filas en las que se busca, positivo o negativo, en la variable a la que apunta _lRowCount_. En operaciones ordinarias, debe devolver el mismo valor para _lplRowsSought_ como se pasó para _lRowCount_, a menos que la búsqueda haya alcanzado el principio o el final de la tabla. 
  
No establezca _lRowCount_ en un número mayor que 50. Para buscar un número mayor de filas, use el método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProcessor. cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI usa el método **IMAPITable:: SeekRow** para localizar el principio de la tabla antes de procesarla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

