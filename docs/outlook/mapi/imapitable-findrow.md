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
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429575"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la siguiente fila de una tabla que coincide con criterios de búsqueda específicos y mueve el cursor a esa fila.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in] Puntero a una [estructura SRestriction](srestriction.md) que describe los criterios de búsqueda. 
    
 _BkOrigin_
  
> [in] Marcador que identifica la fila en la que **FindRow** debe comenzar su búsqueda. Se puede crear un marcador mediante el método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Busca desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Busca en la fila de la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Busca desde el final de la tabla. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la dirección de la búsqueda. Se puede establecer la siguiente marca:
    
DIR_BACKWARD 
  
> Busca hacia atrás desde la fila identificada por el marcador.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se ha realizado correctamente.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador del  _parámetro BkOrigin_ no es válido porque se ha quitado o porque está más allá de la última fila solicitada. 
    
MAPI_E_NOT_FOUND 
  
> No se encontraron filas que coincidan con la restricción.
    
MAPI_W_POSITION_CHANGED
  
> La llamada se ha hecho correctamente, pero el marcador usado en la operación ya no se establece en la misma fila que cuando se usó por última vez; si no se ha usado el marcador, ya no está en la misma posición que cuando se creó. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Consulte [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::FindRow** localiza la primera fila de la tabla para que coincida con un conjunto de criterios de búsqueda descritos en la estructura **SRestriction** a la que apunta el parámetro _lpRestriction._ 
  
Por lo general, **FindRow** busca hacia delante desde el marcador especificado. El autor de la llamada puede establecer la búsqueda para que se mueva hacia atrás desde el marcador estableciendo la marca DIR_BACKWARD en el _parámetro ulFlags._ La búsqueda hacia delante comienza desde el marcador actual; la búsqueda hacia atrás comienza desde la fila anterior al marcador. La posición final de la búsqueda es justo antes de que se encontrara la primera fila que satisficía la restricción. 
  
Si la fila señalada por el marcador en el parámetro  _BkOrigin_ ya no existe en la tabla y la tabla no puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_E_INVALID_BOOKMARK. Si la fila señalada por  _BkOrigin_ ya no existe y la tabla puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_W_POSITION_CHANGED. 
  
Si el marcador pasado en  _BkOrigin_ es BOOKMARK_BEGINNING o BOOKMARK_END, **FindRow** devuelve MAPI_E_NOT_FOUND si no se encuentra ninguna fila que coincida. Si el marcador usado en  _BkOrigin_ es BOOKMARK_CURRENT, **FindRow** puede devolver MAPI_W_POSITION_CHANGED pero no MAPI_E_INVALID_BOOKMARK porque siempre hay una posición del cursor actual. 
  
La **columna de propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) es necesaria para todas las tablas y todas las implementaciones de **FindRow** son necesarias para admitir llamadas que buscan una fila basada en PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El tipo de búsqueda de prefijos realizada por **FindRow** solo es útil cuando la búsqueda sigue la misma dirección que la organización de la tabla. Para lograr el comportamiento necesario, la función de comparación implícita por el **RELOP_GE** pasado en la estructura de restricción de propiedades debe ser la misma función de comparación en la que se basa el criterio de ordenación de tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **FindRow para** admitir el desplazamiento en función de las cadenas que escriba el usuario, especialmente en cuadros de lista dentro de cuadros de diálogo de direcciones. En este tipo de desplazamiento, los usuarios escriben prefijos progresivamente más largos de un valor de cadena deseado y puede emitir periódicamente una llamada **FindRow** para saltar a la primera fila que coincida con el prefijo. La dirección en la que salta el cursor depende de la dirección en la que se establezca la búsqueda para ejecutarse. 
  
Para usar **FindRow,** se debe establecer un marcador. La búsqueda de cadena puede originarse a partir de cualquier marcador, incluidos los marcadores preestablecidos que indican la posición actual y el principio y el final de la tabla. Si hay un gran número de filas en la tabla, la operación de búsqueda puede ser lenta.
  
Use una restricción para buscar un prefijo de cadena para desplazarse de la siguiente manera. Para la búsqueda hacia delante en una columna ordenada en orden ascendente y para la búsqueda hacia atrás en una columna ordenada en orden descendente, pase una estructura  de restricción de propiedades en el parámetro _lpRestriction_ con la relación **RELOP_GE** y la etiqueta y el prefijo de propiedad adecuados, usando el prefijo **GE** de la etiqueta de formato _._ 
  
Para obtener más información acerca del uso de estructuras de restricción para especificar un filtro, vea [Acerca de las restricciones](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el **método IMAPITable::FindRow** para buscar filas que coincidan con una restricción.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

