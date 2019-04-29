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

## <a name="parameters"></a>Parameters

 _lRowCount_
  
> a Número máximo de filas que se van a devolver.
    
 _ulFlags_
  
> a Máscara de caracteres de marcas que controlan cómo se devuelven las filas. Se puede establecer la siguiente marca:
    
TBL_NOADVANCE 
  
> Impide que el cursor avance como resultado de la recuperación de la fila. Si se establece la marca TBL_NOADVANCE, el cursor apunta a la primera fila devuelta. Si no se establece la marca TBL_NOADVANCE, el cursor apunta a la fila que sigue a la última fila devuelta.
    
 _lppRows_
  
> contempla Puntero a un puntero a una estructura [SRowSet](srowset.md) que contiene las filas de la tabla. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas se devolvieron correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de recuperación de filas. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_INVALID_PARAMETER 
  
> El parámetro _IRowCount_ se establece en cero. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: QueryRows** obtiene una o varias filas de datos de una tabla. El valor del parámetro _IRowCount_ afecta al punto inicial de la recuperación. Si _IRowCount_ es positivo, las filas se leen en dirección hacia delante, comenzando en la posición actual. Si _IRowCount_ es negativo, **QueryRows** restablece el punto inicial desplazándose hacia atrás el número indicado de filas. Una vez restablecido el cursor, las filas se leen en orden de reenvío. 
  
El **** miembro Crows de la estructura [SRowSet](srowset.md) apuntado por el parámetro _lppRows_ indica el número de filas devueltas. Si se devuelven cero filas: 
  
- El cursor ya estaba situado al principio de la tabla y el valor de _IRowCount_ es negativo. O 
    
- El cursor ya estaba situado al final de la tabla y el valor de _IRowCount_ es positivo. 
    
El número de columnas y su ordenación son los mismos para cada fila. Si una propiedad no existe para una fila o se produce un error al leer una propiedad, la estructura **SPropValue** de la propiedad en la fila contiene los siguientes valores: 
  
- PT_ERROR para el tipo de propiedad en el miembro **ulPropTag** . 
    
- MAPI_E_NOT_FOUND para el miembro **Value** . 
    
La memoria usada para las estructuras [SPropValue](spropvalue.md) en el conjunto de filas al que apunta el parámetro _lppRows_ debe asignarse por separado y liberarse para cada fila. Use [MAPIFreeBuffer](mapifreebuffer.md) para liberar las estructuras de valores de propiedad y liberar el conjunto de filas. Sin embargo, cuando una llamada a **QueryRows** devuelve cero, lo que indica el principio o el final de la tabla, solo es necesario liberar la propia estructura **SRowSet** . Para obtener más información acerca de cómo asignar y liberar memoria en una estructura **SRowSet** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
Las filas que se devuelven y el orden en que se devuelven dependen de si se han realizado o no llamadas correctas a [IMAPITable:: Restrict](imapitable-restrict.md) y [IMAPITable:: SortTable](imapitable-sorttable.md). **Restringir** las filas de filtros de la vista, lo que hace que **QueryRows** devuelva sólo las filas que coinciden con los criterios especificados en la restricción. **SortTable** establece un criterio de ordenación estándar o categorizado, que afecta a la secuencia de filas devueltas por **QueryRows**. Las filas devueltas están en el orden especificado en la estructura [SSortOrderSet](ssortorderset.md) que se pasa a **SortTable**.
  
Las columnas devueltas para cada fila y el orden en que se devuelven dependen de si se realizó o no una llamada correcta a [IMAPITable:: SetColumns](imapitable-setcolumns.md). **SetColumns** establece un conjunto de columnas que especifica las propiedades que se incluirán en las columnas de la tabla y el orden en que deben incluirse. Si se ha realizado una llamada de **SetColumns** , las columnas determinadas de cada fila y el orden de esas columnas coinciden con el conjunto de columnas especificado en la llamada. Si no se ha realizado ninguna llamada de **SetColumns** , la tabla devuelve el conjunto de columnas predeterminado. 
  
Si no se ha realizado ninguna de estas llamadas, **QueryRows** devuelve todas las filas de la tabla. Cada fila contiene el conjunto de columnas predeterminado en el orden predeterminado. 
  
Cuando el conjunto de columnas establecido en una llamada a [IMAPITable:: SetColumns](imapitable-setcolumns.md) incluye columnas establecidas en PR_NULL, la matriz [SPropValue](spropvalue.md) dentro del conjunto de filas devuelto en _lppRows_ contendrá ranuras vacías. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede permitir que un llamador solicite una columna no admitida que se incluirá en el conjunto de columnas. Cuando esto ocurre, se colocan PT_ERROR en la parte de tipo de propiedad de la etiqueta de propiedad y MAPI_E_NOT_FOUND en el valor de la propiedad para la columna no admitida. 
  
Trate el recuento de filas como una solicitud en lugar de un requisito. Puede devolver cualquier parte de cero filas, si no hay ninguna fila en la dirección de la consulta, al número solicitado. 
  
Devuelve solo las filas que el usuario verá cuando se solicitan filas de una vista de tabla clasificada, lo que permite al autor de la llamada realizar suposiciones válidas sobre el ámbito de los datos y evitar el trabajo adicional. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Por lo general, acabará con tantas filas como ha especificado en el parámetro _lRowCount_ . Sin embargo, cuando los límites de memoria o de implementación son un problema o cuando la operación alcanza el principio o el final de la tabla de forma prematura, **QueryRows** devolverá menos filas de las solicitadas. 
  
Si **QueryRows** devuelve MAPI_E_BUSY, llame al método [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) y vuelva a intentar la llamada a **QueryRows** cuando se complete la operación asincrónica. 
  
Al llamar a **QueryRows**, tenga en cuenta que el tiempo de las notificaciones asincrónicas puede provocar potencialmente que el conjunto de filas que se obtiene de **QueryRows** no represente con precisión los datos subyacentes. Por ejemplo, una llamada a **QueryRows** a la tabla de contenido de una carpeta tras la eliminación de un mensaje, pero antes de la recepción de la notificación correspondiente hará que la fila eliminada se devuelva en el conjunto de filas. Espere siempre a que llegue una notificación antes de actualizar la vista del usuario de los datos. 
  
Para obtener más información acerca de la recuperación de filas de tablas, vea [recuperar datos de filas de tabla](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **IMAPITable:: QueryRows** para recuperar las filas de la tabla que se van a cargar en la vista.  <br/> |
   
## <a name="see-also"></a>Ver también



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

