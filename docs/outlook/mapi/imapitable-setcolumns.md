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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416352"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define las propiedades y el orden de las propiedades específicas que aparecerán como columnas en la tabla.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> a Puntero a una matriz de etiquetas de propiedad que identifican las propiedades que se van a incluir como columnas en la tabla. La parte de tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para adiciones posteriores. El parámetro _lpPropTagArray_ no puede establecerse en null; todas las tablas deben tener al menos una columna. 
    
 _ulFlags_
  
> a Máscara de la máscara que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación. Se pueden establecer los siguientes indicadores: 
    
TBL_ASYNC 
  
> Solicita que la operación de configuración de columna se realice de forma asincrónica, lo que provoca que **SetColumns** pueda devolver potencialmente antes de que la operación se haya completado completamente. 
    
TBL_BATCH 
  
> Permite a la tabla posponer la operación de configuración de columna hasta que se necesiten los datos en realidad.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de configuración de columna se realizó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de configuración de columna. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
## <a name="remarks"></a>Comentarios

El conjunto de columnas de una tabla es el grupo de propiedades que componen las columnas de las filas de la tabla. Hay un conjunto de columnas predeterminado para cada tipo de tabla. El conjunto de columnas predeterminado se compone de las propiedades que incluye automáticamente el implementador de la tabla. Tabla los usuarios pueden modificar este conjunto predeterminado llamando al método **IMAPITable:: SetColumns** . Pueden solicitar que se agreguen otras columnas al conjunto predeterminado si el implementador de la tabla es compatible con las columnas que se van a quitar o el orden de las columnas que se va a cambiar. **SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila. 
  
El éxito de la operación de **SetColumns** sólo es aparente después de realizar una llamada posterior para recuperar los datos de la tabla. Entonces, se informa de que se han producido errores. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Algunos proveedores permiten la llamada de **SetColumns** para ordenar sólo las columnas de la tabla que forman parte de las columnas disponibles para una vista de tabla. Otros proveedores permiten una llamada de **SetColumns** para ordenar todas las columnas de la tabla, incluidas las que contienen propiedades que no están en el conjunto de columnas original. 
  
Cuando TBL_BATCH se establece para operaciones asincrónicas, los proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de propiedad NULL para las columnas que no son compatibles.
  
No es necesario que responda a la marca TBL_ASYNC que solicita que la operación sea asincrónica. Si no admite la definición de conjunto de columnas asincrónica, realice la operación de forma sincrónica. Si puede admitir la marca TBL_ASYNC y hay otra operación asincrónica todavía en curso, devuelva MAPI_E_BUSY. De lo contrario, devuelva S_OK independientemente de si se admiten todas las propiedades incluidas en la matriz de etiquetas de propiedades. Los errores resultantes de propiedades no admitidas deben devolverse desde los métodos de **IMAPITable** que recuperan datos, como **QueryRows**. 
  
No genere notificaciones para las filas de tabla que están ocultas para que las llamadas a **Restrict**se vean. 
  
Al enviar notificaciones de tabla, el orden de las propiedades del miembro de **fila** de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada de **SetColumns** más reciente deben ser iguales a la hora de la solicitud de notificación. se ha enviado. 
  
Otra marca, TBL_BATCH, permite a los llamadores especificar que el implementador de la tabla puede aplazar la evaluación de los resultados de la operación hasta un momento posterior. Siempre que sea posible, los autores de la llamada deben establecer esta marca porque la operación por lotes mejora el rendimiento.
  
A menudo es conveniente que los autores de las llamadas reserven algunas columnas del conjunto de filas recuperadas para los valores que se van a agregar más adelante. Para ello, los autores de las llamadas colocan **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en las posiciones deseadas en la matriz de etiquetas de propiedad pasada a **SetColumns**; a continuación, la tabla devolverá **PR_NULL** en las posiciones de todas las filas recuperadas con **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Al crear la matriz de etiquetas de propiedad para el parámetro _lpPropTagArray_ , ordene las etiquetas en el orden en que desea que aparezcan las columnas en la vista de tabla. 
  
Puede especificar propiedades multivalor para incluirlas en el conjunto de columnas aplicando la marca de instancia multivalor o constante MVI_FLAG a la etiqueta de propiedad. Establezca esta marca pasando la etiqueta de propiedad para la versión de un solo valor de la propiedad como un parámetro a la macro MVI_PROP de la siguiente manera:
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP definirá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta con varios valores. Si intenta llamar erróneamente a MVI_PROP en una propiedad de un solo valor, MAPI omitirá la llamada y dejará sin cambios la etiqueta de propiedad. 
  
Puede incluir etiquetas de propiedad establecidas en **PR_NULL** en la matriz de etiquetas de propiedad para reservar espacio en el conjunto de columnas. El espacio de reserva le permite agregar a un conjunto de columnas sin tener que asignar una nueva matriz de etiquetas de propiedades. 
  
Cuando la llamada a **SetColumns** provoca un cambio en el orden de las columnas de una tabla y una o más de estas columnas representa una propiedad multivalor, es posible que aumente el número de filas de la tabla. Si esto ocurre, se descartan todos los marcadores de la tabla. Para obtener más información acerca de cómo las columnas multivalor afectan a las tablas, vea [Working with](working-with-multivalued-columns.md)multiValued Columns.
  
Establecer columnas es una operación sincrónica de forma predeterminada. Sin embargo, puede permitir que la tabla posponga la operación hasta el momento en que se necesiten los datos mediante la configuración de la marca TBL_BATCH. La configuración de esta marca puede mejorar el rendimiento. Otra marca, TBL_ASYNC, hace que la operación sea asincrónica, lo que permite que **SetColumns** vuelva antes de que se complete la operación. Para determinar cuándo se produce la finalización, llame al [IMAPITable:: getStatus](imapitable-getstatus.md).
  
Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, que indica que otra operación impide que se inicie la operación, puede llamar al método [IMAPITable:: ABORT](imapitable-abort.md) para detener la operación en curso. 
  
También puede llamar a [HrAddColumnsEx](hraddcolumnsex.md) para cambiar un conjunto de columnas. La diferencia entre **HrAddColumnsEx** y **IMAPITable:: SetColumns** es que **HrAddColumnsEx** es menos flexible; solo puede Agregar columnas. Las columnas adicionales se colocan al principio del conjunto de columnas; todas las columnas existentes aparecen a continuación de estas columnas. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa el método **IMAPITable:: SetColumns** para establecer las columnas deseadas para la tabla.  <br/> |
   
## <a name="see-also"></a>Ver también



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

