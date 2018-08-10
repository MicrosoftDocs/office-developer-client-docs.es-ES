---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817586"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Hace referencia a**: Outlook 
  
Busca la siguiente fila en una tabla que coincide con los criterios de búsqueda específicos y mueve el cursor a esa fila.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpRestriction_
  
> [entrada] Un puntero a una estructura [SRestriction](srestriction.md) que se describe los criterios de búsqueda. 
    
 _BkOrigin_
  
> [entrada] Un marcador que identifica la fila donde **FindRow** debe comenzar su búsqueda. Un marcador se puede crear mediante el método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) , o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Búsquedas desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Búsquedas de la fila en la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Búsquedas desde el final de la tabla. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la dirección de la búsqueda. Se puede establecer la marca siguiente:
    
DIR_BACKWARD 
  
> Busca hacia atrás desde la fila identificada por el marcador.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda realizada correctamente.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador en el parámetro _BkOrigin_ no es válido porque se ha eliminado o porque es más allá de la última fila solicitada. 
    
MAPI_E_NOT_FOUND 
  
> Se han encontrado ninguna fila que coincida con la restricción.
    
MAPI_W_POSITION_CHANGED
  
> La llamada se ha realizado correctamente, pero ya no se establece el marcador utilizado en la operación en la misma fila que cuando se usó por última vez; Si no se ha usado el marcador, ya no es en la misma posición que cuando se creó. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Vea [uso de Macros para el tratamiento de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: FindRow** busca la primera fila de la tabla para que coincida con un conjunto de criterios de búsqueda que se describen en la estructura de **SRestriction** indicada por el parámetro _lpRestriction_ . 
  
Normalmente, **FindRow** busca hacia delante desde el marcador especificado. El llamador puede establecer la búsqueda hacia atrás desde el marcador estableciendo el indicador DIR_BACKWARD en el parámetro _ulFlags indicado_ . Buscar hacia delante se inicia desde el marcador actual; Buscar hacia atrás comienza a partir de la fila antes de marcador. La posición final de la búsqueda es justo antes de la primera fila que se encuentra que cumplen la restricción. 
  
Si la fila indicada por el marcador en el parámetro _BkOrigin_ ya no existe en la tabla y la tabla no puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_E_INVALID_BOOKMARK. Si la fila que apunta _BkOrigin_ ya no existe y la tabla es capaz de establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_W_POSITION_CHANGED. 
  
Si el marcador se pasan en _BkOrigin_ es BOOKMARK_BEGINNING o BOOKMARK_END, **FindRow** devuelve MAPI_E_NOT_FOUND si no se encuentra ninguna fila coincidente. Si el marcador utilizado en _BkOrigin_ es BOOKMARK_CURRENT, **FindRow** puede devolver MAPI_W_POSITION_CHANGED pero no MAPI_E_INVALID_BOOKMARK debido a que siempre hay una posición del cursor actual. 
  
La columna de la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) es obligatoria para todas las tablas y todas las implementaciones de **FindRow** son necesarios para admitir las llamadas que busquen una fila basada en PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

El tipo de prefijo buscar realizado por **FindRow** sólo es útil cuando la búsqueda sigue la misma dirección que la organización de la tabla. Con el fin de lograr el comportamiento necesario, la función de comparación implicada por la **RELOP_GE** se pasan en la estructura de la restricción de propiedad debe ser la misma función de comparación en la que se basa el criterio de ordenación de la tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **FindRow** para admitir el desplazamiento en función de las cadenas escritas por el usuario, especialmente en los cuadros de lista dentro de los cuadros de diálogo de dirección. En este tipo de desplazamiento, los usuarios escriben prolonga prefijos de un valor de cadena que desee y, periódicamente puede emitir una llamada **FindRow** para saltar a la primera fila que coincide con el prefijo. Qué dirección salta el cursor depende de la dirección de la búsqueda se establece para ejecutarse. 
  
Para usar **FindRow**, se debe establecer un marcador. La búsqueda de cadenas puede proceder de cualquier marcador, incluidos los de los marcadores predefinidos que indica la posición actual y el principio y el final de la tabla. Si hay un gran número de filas de la tabla, la operación de búsqueda puede ser lenta.
  
Use una restricción para buscar un prefijo de cadena para el desplazamiento de la siguiente manera. Para buscar hacia delante en una columna que se ordenan en orden ascendente y para las búsquedas con versiones anteriores en una columna que se ordenan en orden descendente, pase una estructura de restricción de propiedad en el parámetro _lpRestriction_ con la relación **RELOP_GE** y el correspondiente etiqueta de la propiedad y el prefijo, con _el formato **GE** _prefijo__ . 
  
Para obtener más información acerca del uso de las estructuras de restricción para especificar un filtro, vea el tema [Acerca de las restricciones](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **IMAPITable:: FindRow** para buscar las filas que coinciden con una restricción.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

