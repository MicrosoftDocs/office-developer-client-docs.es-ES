---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817601"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Se aplica a**: Outlook 
  
Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [entrada] Puntero a una matriz de etiquetas de propiedad que identifica las propiedades que se incluirán como columnas de la tabla. La parte de tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para adiciones posteriores. El parámetro _lpPropTagArray_ no puede establecerse en NULL; cada tabla debe tener al menos una columna. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación. Se pueden establecer los siguientes indicadores: 
    
TBL_ASYNC 
  
> Las solicitudes que la operación de configuración de columna realizan asincrónicamente causando **SetColumns** devolver potencialmente antes de la operación ha finalizado completamente. 
    
TBL_BATCH 
  
> Permite a la tabla para posponer la operación de configuración de la columna hasta que los datos se necesita realmente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de configuración de columna fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la columna Configuración de la operación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
## <a name="remarks"></a>Notas

El conjunto de columnas de una tabla es el grupo de propiedades que componen las columnas para las filas de la tabla. No hay una columna predeterminado establecido para cada tipo de tabla. El conjunto de columnas predeterminado se compone de las propiedades que el implementador de la tabla incluye automáticamente. Los usuarios de la tabla pueden modificar este valor predeterminado que se establece mediante una llamada al método **IMAPITable::SetColumns** . Puede solicitar que otras columnas se agregará al conjunto si el implementador de la tabla es compatible con ellos que pueden quitar columnas o que se puede cambiar el orden de columnas predeterminado. **SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila. 
  
El éxito de la operación **SetColumns** es evidente sólo después de que se ha realizado una llamada posterior para recuperar los datos de la tabla. A continuación, es que los errores se notifican. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Algunos proveedores permiten una llamada **SetColumns** ordenar sólo columnas de la tabla que forman parte de las columnas disponibles para una vista de tabla. Otros proveedores de permiten una llamada **SetColumns** ordenar todas las columnas de tabla, incluidas aquellas que contienen propiedades no en el conjunto de columna original. 
  
Cuando se establece TBL_BATCH para operaciones asincrónicas, proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de la propiedad null para las columnas que no son compatibles.
  
No es necesario responder a la solicitud de marca TBL_ASYNC que la operación de ser asincrónica. Si no admite la definición del conjunto de columna asincrónica, realizar la operación de forma sincrónica. Si puede admitir la marca TBL_ASYNC y otro asincrónica operación todavía está en progreso, MAPI_E_BUSY devuelto. De lo contrario, devuelve S_OK, independientemente de si o no admiten todas las propiedades que se incluyen en la matriz de la etiqueta de propiedad. Desde métodos **IMAPITable** que recuperar datos, como **QueryRows**se deben devolver errores resultante de propiedades no son compatibles. 
  
No generan notificaciones para las filas de tabla que están ocultos de la vista mediante llamadas a **restringir**. 
  
Al enviar las notificaciones de tabla, el orden de las propiedades en el miembro de **fila** de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada más reciente de **SetColumns** debe ser el mismo a partir de la hora en que la notificación de solicitud se ha enviado. 
  
Otro indicador, TBL_BATCH, permite que los autores de llamadas especificar que el implementador de tabla puede aplazar la evaluación de los resultados de la operación hasta más adelante. Siempre que sea posible, los autores de llamadas deben establecer esta marca debido a que la operación por lotes mejora el rendimiento.
  
A menudo es conveniente para los autores de llamadas reservar algunas columnas en el conjunto de filas devueltas para los valores que se agregarán más adelante. Los autores de llamadas hacer esto mediante la colocación de **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en la posición que desee en la matriz de etiqueta de propiedad que se pasan a **SetColumns**; en la tabla será, a continuación, pase a la copia **PR_NULL** en las posiciones de todas las filas recuperadas con **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Al crear la matriz de la etiqueta de propiedad para el parámetro _lpPropTagArray_ , orden de las etiquetas en el orden que desea que las columnas que aparecen en la vista de tabla. 
  
Puede especificar propiedades multivalor que se deben incluir en la columna establecer aplicando el indicador de instancia multivalor o constante MVI_FLAG, en la etiqueta de propiedad. Establezca esta marca pasando la etiqueta de propiedad para la versión de un solo valor de la propiedad como un parámetro a la macro MVI_PROP como se indica a continuación:
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP establecerá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta multivalor. Si intenta llamar a MVI_PROP en una propiedad de un solo valor erróneamente, MAPI omitir la llamada y deje la etiqueta de propiedad sin cambios. 
  
Puede incluir etiquetas de propiedad se establece en **PR_NULL** en la matriz de la etiqueta de propiedad para reservar espacio en el conjunto de columnas. Reservar espacio permite agregar a una columna establecer sin tener que volver a asignar una matriz de etiqueta de propiedad nuevo. 
  
Cuando la llamada a **SetColumns** hace que un cambio al orden de las columnas de una tabla y una o varias de estas columnas representan una propiedad multivalor, es posible que el número de filas de la tabla para aumentar. Si esto ocurre, se descartan todos los marcadores de la tabla. Para obtener más información acerca de cómo columnas con varios valores afectan a las tablas, vea [trabajar con columnas con varios valores](working-with-multivalued-columns.md).
  
Configuración de columnas predeterminada es una operación sincrónica. Sin embargo, puede permitir que la tabla que se va a posponer la operación hasta que se necesitan los datos mediante la configuración de la marca TBL_BATCH. Al establecer este indicador puede mejorar el rendimiento. Otro indicador, TBL_ASYNC, hace que la operación asincrónica, lo que permite **SetColumns** devolver antes de completar la operación. Para determinar cuándo se produce la finalización, llame a [IMAPITable::GetStatus](imapitable-getstatus.md).
  
Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, que indica que otra operación impide que la operación de inicio, se puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la operación en curso. 
  
También puede llamar a [HrAddColumnsEx](hraddcolumnsex.md) para cambiar un conjunto de columnas. La diferencia entre **HrAddColumnsEx** y **IMAPITable::SetColumns** es que **HrAddColumnsEx** es menos flexible; sólo puede agregar columnas. Las columnas adicionales se colocan al principio del conjunto de columna; todas las columnas existentes aparecen a continuación de estas columnas. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI usa el método **IMAPITable::SetColumns** para establecer las columnas de la tabla que desee.  <br/> |
   
## <a name="see-also"></a>Ver también



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable:: QueryRows](imapitable-queryrows.md)
  
[IMAPITable:: Restrict](imapitable-restrict.md)
  
[SortTable](imapitable-sorttable.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

