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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329087"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la siguiente fila de una tabla que coincida con los criterios de búsqueda específicos y mueve el cursor a esa fila.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> a Un puntero a una estructura [SRestriction](srestriction.md) que describe los criterios de búsqueda. 
    
 _BkOrigin_
  
> a Un marcador que identifica la fila en la que **FindRow** debe comenzar su búsqueda. Un marcador se puede crear con el método [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos. 
    
BOOKMARK_BEGINNING 
  
> Busca desde el principio de la tabla. 
    
BOOKMARK_CURRENT 
  
> Busca desde la fila de la tabla donde se encuentra el cursor. 
    
BOOKMARK_END 
  
> Busca desde el final de la tabla. 
    
 _ulFlags_
  
> a Una máscara de direcciones de marcas que controla la dirección de la búsqueda. Se puede establecer la siguiente marca:
    
DIR_BACKWARD 
  
> Busca hacia atrás a partir de la fila identificada por el marcador.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de búsqueda se realizó correctamente.
    
MAPI_E_INVALID_BOOKMARK 
  
> El marcador del parámetro _BkOrigin_ no es válido porque se quitó o porque está más allá de la última fila solicitada. 
    
MAPI_E_NOT_FOUND 
  
> No se encontró ninguna fila que coincidiera con la restricción.
    
MAPI_W_POSITION_CHANGED
  
> La llamada se realizó correctamente, pero el marcador usado en la operación ya no se establece en la misma fila que la última vez que se usó; Si no se ha utilizado el marcador, deja de estar en la misma posición que cuando se creó. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Consulte [uso de macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: FindRow** busca la primera fila de la tabla para que sea igual a un conjunto de criterios de búsqueda descrito en la estructura **SRestriction** apuntado por el parámetro _lpRestriction_ . 
  
Normalmente, las búsquedas **FindRow** avanzan desde el marcador especificado. El autor de la llamada puede configurar la búsqueda para desplazarse hacia atrás desde el marcador estableciendo la marca DIR_BACKWARD en el parámetro _ulFlags_ . La búsqueda hacia delante comienza a partir del marcador actual; la búsqueda hacia atrás comienza a partir de la fila anterior al marcador. La posición final de la búsqueda es justo antes de que se haya encontrado la primera fila que satisfizo la restricción. 
  
Si la fila a la que apunta el marcador en el parámetro _BkOrigin_ ya no existe en la tabla y la tabla no puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_E_INVALID_BOOKMARK. Si la fila a la que apunta _BkOrigin_ ya no existe y la tabla puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_W_POSITION_CHANGED. 
  
Si el marcador pasado en _BkOrigin_ es BOOKMARK_BEGINNING o BOOKMARK_END, **FindRow** devuelve MAPI_E_NOT_FOUND si no se encuentra ninguna fila coincidentes. Si el marcador usado en _BkOrigin_ es BOOKMARK_CURRENT, **FINDROW** puede devolver MAPI_W_POSITION_CHANGED pero no MAPI_E_INVALID_BOOKMARK porque siempre hay una posición del cursor actual. 
  
La columna de propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) es necesaria para todas las tablas y todas las implementaciones de **FindRow** son necesarias para admitir llamadas que buscan una fila basada en PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El tipo de prefijo de búsqueda realizado por **FindRow** solo es útil cuando la búsqueda sigue la misma dirección que la organización de tabla. Para lograr el comportamiento necesario, la función de comparación que implica la **RELOP_GE** que se pasa en la estructura de restricción de propiedad debe ser la misma función de comparación en la que se basa el criterio de ordenación de la tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **FindRow** para admitir el desplazamiento en función de las cadenas escritas por el usuario, especialmente en los cuadros de lista de los cuadros de diálogo de dirección. En este tipo de desplazamiento, los usuarios especifican prefijos más largos de un valor de cadena deseado y puede emitir periódicamente una llamada **FindRow** para saltar a la primera fila que coincide con el prefijo. La dirección que salta el cursor depende de la dirección en la que se establece que se ejecute la búsqueda. 
  
Para usar **FindRow**, se debe establecer un marcador. La búsqueda de cadena puede provenir de cualquier marcador, incluidos los marcadores preestablecidos que indican la posición actual y el principio y el final de la tabla. Si hay un gran número de filas en la tabla, la operación de búsqueda puede ser lenta.
  
Use una restricción para buscar un prefijo de cadena para el desplazamiento, como se indica a continuación. Para que la búsqueda hacia delante en una columna se ordene en orden ascendente y para que la búsqueda hacia atrás en una columna se ordene en orden descendente, pase una estructura de restricción de propiedad en el parámetro _lpRestriction_ con la relación **RELOP_GE** y el correspondiente. etiqueta de propiedad y prefijo, con el prefijo _etiqueta_ de formato **GE** __. 
  
Para obtener más información acerca del uso de estructuras de restricción para especificar un filtro, consulte [About Restrictions](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **IMAPITable:: FindRow** para buscar filas que coinciden con una restricción.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

