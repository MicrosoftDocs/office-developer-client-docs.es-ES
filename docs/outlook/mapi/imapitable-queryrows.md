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
ms.openlocfilehash: 179d76b56c1ba9b40768c691d0b1555377f7adb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595051"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve una o varias filas de una tabla, que comienza en la posición actual del cursor.
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parámetros

 _lRowCount_
  
> [entrada] Número máximo de filas que se va a devolver.
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controlan cómo se devuelven filas. Se puede establecer la marca siguiente:
    
TBL_NOADVANCE 
  
> Impide que el cursor avance como consecuencia de la recuperación de filas. Si se establece la marca TBL_NOADVANCE, devuelven los puntos de cursor a la primera fila. Si no está establecido el indicador TBL_NOADVANCE, el cursor señala a la fila que sigue a la última fila devuelta.
    
 _lppRows_
  
> [out] Puntero a un puntero a una estructura [SRowSet](srowset.md) que contiene las filas de tabla. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas correctamente se han devuelto.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de recuperación de la fila de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_INVALID_PARAMETER 
  
> El parámetro _IRowCount_ se establece en cero. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: QueryRows** Obtiene una o varias filas de datos de una tabla. El valor del parámetro _IRowCount_ influye en el punto de partida para la recuperación. Si _IRowCount_ es positivo, se leen las filas hacia delante, comenzando en la posición actual. Si _IRowCount_ es negativo, **QueryRows** restablece el punto de partida moviendo hacia atrás el número de filas indicado. Después de restablece el cursor, se leen las filas en orden hacia delante. 
  
El miembro **cRows** en la estructura de [SRowSet](srowset.md) indicada por el parámetro _lppRows_ indica el número de filas devueltas. Si se devuelven cero filas: 
  
- Ya se ha colocado el cursor al principio de la tabla y el valor de _IRowCount_ es negativo. - O - 
    
- Ya se ha colocado el cursor al final de la tabla y el valor de _IRowCount_ es positivo. 
    
El número de columnas y su ordenación es el mismo para cada fila. Si no existe una propiedad de una fila o hay un error al leer una propiedad, la estructura de **SPropValue** para la propiedad en la fila contiene los siguientes valores: 
  
- PT_ERROR para el tipo de propiedad en el miembro **ulPropTag** . 
    
- MAPI_E_NOT_FOUND para el miembro de **valor** . 
    
Memoria usada para las estructuras [SPropValue](spropvalue.md) en el conjunto de filas que apunta el parámetro _lppRows_ debe ser asignado y liberan para cada fila por separado. Utilice [MAPIFreeBuffer](mapifreebuffer.md) para liberar las estructuras de valor de propiedad y para liberar la fila establezca. Cuando una llamada a **QueryRows** devuelve cero, sin embargo, que indica al principio o al final de la tabla, la estructura de **SRowSet** propio debe liberarse. Para obtener más información acerca de cómo asignar y liberar memoria en una estructura **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
Las filas que se devuelven y el orden en el que se devuelven dependen de si [IMAPITable:: Restrict](imapitable-restrict.md) y [SortTable](imapitable-sorttable.md)se han realizado llamadas correctas. **Restrict** filtra las filas de la vista, lo que provoca que **QueryRows** devolver sólo las filas que coinciden con los criterios especificados en la restricción. **SortTable** establece un estándar o clasificar el criterio de ordenación, que afectan a la secuencia de filas devueltas por **QueryRows**. Las filas devueltas se encuentran en el orden especificado en la estructura de [SSortOrderSet](ssortorderset.md) que se pasan a **SortTable**.
  
Devuelven las columnas de cada fila y el orden en el que se devuelven dependen de si se realizó una llamada correcta a [IMAPITable::SetColumns](imapitable-setcolumns.md). **SetColumns** establece un conjunto de columnas, la especificación de las propiedades que se deben incluir en las columnas de la tabla y el orden en el que se deben incluir. Si se ha realizado una llamada **SetColumns** , las columnas determinadas en cada fila y el orden de las columnas coinciden con el conjunto especificado en la llamada de columnas. Si se ha realizado ninguna llamada **SetColumns** , en la tabla devuelve su conjunto de columnas predeterminado. 
  
Si se ha realizado ninguna de estas llamadas, **QueryRows** devuelve todas las filas de la tabla. Cada fila contiene la columna predeterminada está establecida en el orden predeterminado. 
  
Cuando el conjunto de columnas establecido en una llamada a [IMAPITable::SetColumns](imapitable-setcolumns.md) incluye columnas establecida en PR_NULL, la matriz [SPropValue](spropvalue.md) dentro del conjunto de filas devuelto en _lppRows_ contendrá ranuras vacías. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede permitir que un autor de la llamada solicitar una columna no compatible que se deben incluir en el conjunto de columnas. Cuando esto ocurre, coloque PT_ERROR en la parte de tipo de propiedad de la etiqueta de propiedad y MAPI_E_NOT_FOUND en el valor de la propiedad para la columna no compatible. 
  
Trata el recuento de filas como una solicitud en lugar de un requisito. Puede devolver en cualquier lugar desde cero filas, si no hay ninguna fila en la dirección de la consulta, en el número solicitado. 
  
Devolver sólo las filas que se muestra al usuario cuando se solicitan las filas de una vista de tabla con categorías, lo que permite el autor de la llamada hacer válidos suposiciones sobre el alcance de los datos y para evitar trabajo adicional. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Normalmente, terminará con un número de filas según lo especificado en el parámetro _lRowCount_ . Sin embargo, cuando los límites de memoria o implementación son un problema o cuando la operación llega al principio o al final de la tabla de forma prematura, **QueryRows** devolverá menos filas que las solicitadas. 
  
Si **QueryRows** devuelve MAPI_E_BUSY, llame al método [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) y vuelva a intentar la llamada a **QueryRows** una vez finalizada la operación asincrónica. 
  
Cuando se llama a **QueryRows**, tenga en cuenta que la sincronización de notificaciones asincrónicas puede causar el conjunto de filas que obtener back de **QueryRows** no para representar con precisión los datos subyacentes. Por ejemplo, se establece una llamada a **QueryRows** a siguiente de tabla de contenido de una carpeta de la eliminación de un mensaje, pero antes de la recepción de la notificación correspondiente hará que la fila eliminada que se devuelve en la fila. Espere siempre una notificación llegar antes de actualizar la vista del usuario de los datos. 
  
Para obtener más información acerca de cómo recuperar filas de tablas, vea [Recuperación de datos de las filas de tabla](retrieving-data-from-table-rows.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **IMAPITable:: QueryRows** para recuperar las filas de la tabla que se va a cargar en la vista.  <br/> |
   
## <a name="see-also"></a>Vea también



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

