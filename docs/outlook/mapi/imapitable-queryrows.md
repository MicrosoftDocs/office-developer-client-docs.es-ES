---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416296"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parámetros

 _lRowCount_
  
> [entrada] Número máximo de filas que se devolverán.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controlan cómo se devuelven las filas. Se puede establecer la siguiente marca:
    
TBL_NOADVANCE 
  
> Impide que el cursor avance como resultado de la recuperación de filas. Si se TBL_NOADVANCE marca, el cursor apunta a la primera fila devuelta. Si no TBL_NOADVANCE marca, el cursor apunta a la fila que sigue a la última fila devuelta.
    
 _lppRows_
  
> [salida] Puntero a un puntero a una [estructura SRowSet](srowset.md) que contiene las filas de la tabla. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas se devolvieron correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de recuperación de filas. La operación en curso debe poder completarse o debe detenerse.
    
MAPI_E_INVALID_PARAMETER 
  
> El  _parámetro IRowCount_ se establece en cero. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::QueryRows** obtiene una o más filas de datos de una tabla. El valor del parámetro  _IRowCount_ afecta al punto de inicio de la recuperación. Si  _IRowCount_ es positivo, las filas se leen en dirección hacia delante, comenzando en la posición actual. Si  _IRowCount_ es negativo, **QueryRows** restablece el punto inicial moviendo hacia atrás el número de filas indicado. Una vez restablecido el cursor, las filas se leen en orden hacia delante. 
  
El **miembro cRows** de la estructura [SRowSet](srowset.md) a la que apunta el parámetro  _lppRows_ indica el número de filas devueltas. Si se devuelven cero filas: 
  
- El cursor ya estaba situado al principio de la tabla y el valor de  _IRowCount_ es negativo. -Or- 
    
- El cursor ya estaba situado al final de la tabla y el valor de  _IRowCount_ es positivo. 
    
El número de columnas y su orden es el mismo para cada fila. Si una propiedad no existe para una fila o hay un error al leer una propiedad, la estructura **SPropValue** de la propiedad de la fila contiene los siguientes valores: 
  
- PT_ERROR para el tipo de propiedad en el **miembro ulPropTag.** 
    
- MAPI_E_NOT_FOUND para el **miembro Value.** 
    
La memoria usada para las [estructuras SPropValue](spropvalue.md) del conjunto de filas al que apunta el parámetro  _lppRows_ debe asignarse y liberarse por separado para cada fila. Usa [MAPIFreeBuffer para](mapifreebuffer.md) liberar las estructuras de valores de propiedad y liberar el conjunto de filas. Sin embargo, cuando una llamada a **QueryRows** devuelve cero, lo que indica el principio o el final de la tabla, solo es necesario liberar la estructura **SRowSet** en sí. Para obtener más información acerca de cómo asignar y liberar memoria en una estructura **SRowSet,** vea Managing [Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Las filas que se devuelven y el orden en que se devuelven dependen de si se han realizado o no llamadas correctas a [IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::SortTable](imapitable-sorttable.md). **Restringir** filtra filas de la vista, lo que hace que **QueryRows** devuelva solo las filas que coinciden con los criterios especificados en la restricción. **SortTable** establece un criterio de ordenación estándar o categorizado, que afecta a la secuencia de filas devueltas por **QueryRows**. Las filas devueltas están en el orden especificado en la estructura [SSortOrderSet](ssortorderset.md) pasada a **SortTable**.
  
Las columnas devueltas para cada fila y el orden en que se devuelven dependen de si se ha realizado o no una llamada correcta a [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** establece un conjunto de columnas, especificando las propiedades que se incluirán en las columnas de la tabla y el orden en que deben incluirse. Si se ha realizado una llamada **a SetColumns,** las columnas concretas de cada fila y el orden de esas columnas coinciden con el conjunto de columnas especificado en la llamada. Si no se ha realizado ninguna llamada a **SetColumns,** la tabla devuelve su conjunto de columnas predeterminado. 
  
Si no se ha realizado ninguna de estas llamadas, **QueryRows** devuelve todas las filas de la tabla. Cada fila contiene la columna predeterminada establecida en orden predeterminado. 
  
Cuando el conjunto de columnas se establece en una llamada a [IMAPITable::SetColumns](imapitable-setcolumns.md) incluye columnas establecidas en PR_NULL, la matriz [SPropValue](spropvalue.md) dentro del conjunto de filas devuelto en _lppRows contendrá ranuras vacías._ 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede permitir que el autor de la llamada solicite que se incluya una columna no admitida en el conjunto de columnas. Cuando esto ocurre, coloque PT_ERROR la parte del tipo de propiedad de la etiqueta de propiedad y MAPI_E_NOT_FOUND en el valor de propiedad de la columna no admitida. 
  
Trate el recuento de filas como una solicitud en lugar de un requisito. Puede volver a cualquier lugar desde cero filas, si no hay filas en la dirección de la consulta, hasta el número solicitado. 
  
Devuelve solo las filas que el usuario verá cuando se soliciten filas desde una vista de tabla categorizada, lo que permite al autor de la llamada hacer suposiciones válidas sobre el ámbito de los datos y evitar trabajo adicional. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Normalmente, terminará con tantas filas como haya especificado en el _parámetro lRowCount._ Sin embargo, cuando los límites de memoria o implementación son un problema o cuando la operación llega al principio o al final de la tabla prematuramente, **QueryRows** devolverá menos filas de las solicitadas. 
  
Si **QueryRows** devuelve MAPI_E_BUSY, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) y vuelva a intentar la llamada a **QueryRows** cuando se complete la operación asincrónica. 
  
Al llamar **a QueryRows,** tenga en cuenta que la sincronización de las notificaciones asincrónicas puede provocar que el conjunto de filas que obtiene de **QueryRows** no represente con precisión los datos subyacentes. Por ejemplo, una llamada a **QueryRows** a la tabla de contenido de una carpeta después de eliminar un mensaje, pero antes de recibir la notificación correspondiente hará que la fila eliminada se devuelva en el conjunto de filas. Espere siempre a que llegue una notificación antes de actualizar la vista del usuario de los datos. 
  
Para obtener más información acerca de cómo recuperar filas de tablas, vea [Recuperar datos de filas de tabla](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el **método IMAPITable::QueryRows** para recuperar filas de la tabla para cargar en la vista.  <br/> |
   
## <a name="see-also"></a>Consulte también



[ADRENTRY](adrentry.md)
  
[FreeProws](freeprows.md)
  
[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

