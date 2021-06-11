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
  
Define las propiedades concretas y el orden de las propiedades que se mostrarán como columnas en la tabla.
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Puntero a una matriz de etiquetas de propiedades que identifican las propiedades que se incluirán como columnas en la tabla. La parte del tipo de propiedad de cada etiqueta se puede establecer en un tipo válido o en **PR_NULL** para reservar espacio para las adiciones posteriores. El  _parámetro lpPropTagArray_ no se puede establecer en NULL; cada tabla debe tener al menos una columna. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la devolución de una llamada asincrónica a **SetColumns**, por ejemplo, cuando se usa **SetColumns** en la notificación. Se pueden establecer las siguientes marcas: 
    
TBL_ASYNC 
  
> Solicita que la operación de configuración de columna se realice de forma asincrónica, lo que hace que **SetColumns** vuelva potencialmente antes de que la operación se haya completado por completo. 
    
TBL_BATCH 
  
> Permite a la tabla posponer la operación de configuración de columna hasta que los datos son realmente necesarios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de configuración de columna se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de configuración de columna. Debe permitirse completar la operación en curso o detenerse.
    
## <a name="remarks"></a>Comentarios

El conjunto de columnas de una tabla es el grupo de propiedades que forma las columnas de las filas de la tabla. Hay un conjunto de columnas predeterminado para cada tipo de tabla. El conjunto de columnas predeterminado está hecho de las propiedades que el implementador de tabla incluye automáticamente. Los usuarios de tabla pueden modificar este conjunto predeterminado llamando al **método IMAPITable::SetColumns.** Pueden solicitar que se agregó otras columnas al conjunto predeterminado si el implementador de tablas las admite para que se quiten las columnas o que se cambie el orden de las columnas. **SetColumns** especifica las columnas que se devuelven con cada fila y el orden de estas columnas dentro de la fila. 
  
El éxito de la **operación SetColumns** solo se muestra después de realizar una llamada posterior para recuperar los datos de la tabla. A continuación, se notifican los errores. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Algunos proveedores permiten que una **llamada SetColumns** ordene solo las columnas de tabla que forman parte de las columnas disponibles para una vista de tabla. Otros proveedores permiten que una **llamada SetColumns** ordene todas las columnas de tabla, incluidas aquellas que contienen propiedades que no están en el conjunto de columnas original. 
  
Cuando TBL_BATCH para operaciones asincrónicas, los proveedores deben devolver un tipo de propiedad de PT_ERROR y un valor de propiedad de NULL para las columnas que no son compatibles.
  
No es necesario responder a la marca TBL_ASYNC que solicita que la operación sea asincrónica. Si no admite la definición de conjunto de columnas asincrónica, realice la operación sincrónicamente. Si puede admitir la marca TBL_ASYNC y otra operación asincrónica todavía está en curso, devuelva MAPI_E_BUSY. De lo contrario, S_OK independientemente de si admite o no todas las propiedades incluidas en la matriz de etiquetas de propiedades. Los errores resultantes de propiedades no admitidas deben devolverse de métodos **IMAPITable** que recuperan datos, como **QueryRows**. 
  
No genere notificaciones para las filas de tabla que están ocultas de la vista mediante llamadas a **Restrict**. 
  
Al enviar notificaciones de tabla, el  orden de las propiedades en el miembro de fila de la estructura [TABLE_NOTIFICATION](table_notification.md) y el orden especificado por la llamada **SetColumns** más reciente debe ser el mismo que en el momento en que se envió la solicitud de notificación. 
  
Otra marca, TBL_BATCH, permite a los autores de llamadas especificar que el implementador de tabla puede aplazar la evaluación de los resultados de la operación hasta una hora posterior. Siempre que sea posible, los autores de llamadas deben establecer esta marca porque la operación por lotes mejora el rendimiento.
  
A menudo es conveniente que los autores de llamadas reserven algunas columnas del conjunto de filas recuperado para que los valores se puedan agregar más adelante. Los autores de llamadas hacen esto **colocando PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) en las posiciones deseadas en la matriz de etiquetas de propiedad pasada a **SetColumns**; a continuación, la tabla pasará **PR_NULL** en esas posiciones en todas las filas recuperadas con **QueryRows**.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Al crear la matriz de etiquetas de propiedad para el parámetro  _lpPropTagArray,_ ordene las etiquetas en el orden en que desea que las columnas aparezcan en la vista de tabla. 
  
Puede especificar propiedades multivalor que se incluirán en el conjunto de columnas aplicando la marca de instancia multivalor o MVI_FLAG constante, a la etiqueta de propiedad. Establezca esta marca pasando la etiqueta de propiedad de la versión de un solo valor de la propiedad como parámetro a la macro MVI_PROP siguiente:
  
```
MVI_PROP(ulPropTag)

```

La macro MVI_PROP establecerá MVI_FLAG para la propiedad, convirtiendo la etiqueta en una etiqueta multivalor. Si intenta llamar erróneamente a MVI_PROP en una propiedad de un solo valor, MAPI omitirá la llamada y dejará la etiqueta de propiedad sin cambios. 
  
Puede incluir etiquetas de propiedad **establecidas en PR_NULL** en la matriz de etiquetas de propiedad para reservar espacio en el conjunto de columnas. Reservar espacio permite agregar a un conjunto de columnas sin tener que asignar una nueva matriz de etiquetas de propiedades. 
  
Cuando la llamada a **SetColumns** provoca un cambio en el orden de las columnas de una tabla y una o más de estas columnas representan una propiedad multivalor, es posible que aumente el número de filas de la tabla. Si esto ocurre, se descartan todos los marcadores de la tabla. Para obtener más información sobre cómo afectan las columnas multivalor a las tablas, vea [Working with Multivalued Columns](working-with-multivalued-columns.md).
  
Establecer columnas es de forma predeterminada una operación sincrónica. Sin embargo, puede permitir que la tabla posponga la operación hasta que los datos se necesiten estableciendo la marca TBL_BATCH datos. Establecer esta marca puede mejorar el rendimiento. Otra marca, TBL_ASYNC, hace que la operación sea asincrónica, lo que permite que **SetColumns** vuelva antes de que se complete la operación. Para determinar cuándo se produce la finalización, llame [a IMAPITable::GetStatus](imapitable-getstatus.md).
  
Si una llamada a **SetColumns** devuelve MAPI_E_BUSY, lo que indica que otra operación impide que se inicie la operación, puede llamar a [IMAPITable::Abort](imapitable-abort.md) para detener la operación en curso. 
  
También puede llamar a [HrAddColumnsEx para](hraddcolumnsex.md) cambiar un conjunto de columnas. La diferencia entre **HrAddColumnsEx** e **IMAPITable::SetColumns** es que **HrAddColumnsEx** es menos flexible; solo puede agregar columnas. Las columnas adicionales se colocan al principio del conjunto de columnas; todas las columnas existentes aparecen después de estas columnas. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI usa el **método IMAPITable::SetColumns** para establecer las columnas deseadas para la tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



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

