---
<<<<<<< Título HEAD: AbsolutePosition (propiedad) (ADO) TOCTitle: AbsolutePosition (propiedad) (ADO) ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: ms.date 48544787: 18/09/2015 mtps_ versión: Office.15
---

# <a name="absoluteposition-property-ado"></a>AbsolutePosition (propiedad, ADO)

=== título: AbsolutePosition (propiedad, ADO) TOCTitle: AbsolutePosition (propiedad, ADO) ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID: ms.date 48544787: 17/10/2018 mtps_version: Office.15
---

# <a name="absoluteposition-property-ado"></a>AbsolutePosition (propiedad, ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indica la posición ordinal del registro actual de un objeto [Recordset](recordset-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de registros del objeto **Recordset** ([RecordCount](recordcount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Comentarios

<<<<<<< HEAD en orden para establecer la propiedad **AbsolutePosition** , ADO requiere que el proveedor OLE DB que esté utilizando implemente la interfaz IRowsetLocate.
=== Para establecer la propiedad **AbsolutePosition** , ADO requiere que el proveedor OLE DB que esté utilizando implemente la interfaz IRowsetLocate.
>>>>>>> master

Al obtener acceso a la propiedad **AbsolutePosition** de un objeto **Recordset** que se ha abierto con un cursor de sólo avance o un cursor dinámico, se genera el error **adErrFeatureNotAvailable**. Con otros tipos de cursor, se devolverá la posición correcta, siempre y cuando el proveedor admita la interfaz IRowsetScroll. Si el proveedor no admite la interfaz *IRowsetScroll*, el valor de la propiedad se establece en **adPosUnknown**. Vea la documentación de su proveedor para determinar si admite *IRowsetScroll*.

Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset** o para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.

Al igual que la propiedad [AbsolutePage](absolutepage-property-ado.md), **AbsolutePosition** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Se puede obtener el número total de registros del objeto **Recordset** mediante la propiedad [RecordCount](recordcount-property-ado.md).

<<<<<<< HEAD cuando se establece la propiedad **AbsolutePosition** , incluso si se va a un registro en la memoria caché actual, ADO vuelve a cargar la memoria caché con un nuevo grupo de registros empezando por el registro especificado. La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.


> [!NOTE]
> <a name="pyou-should-not-use-the-strongabsolutepositionstrong-property-as-a-surrogate-record-number-the-position-of-a-given-record-changes-when-you-delete-a-preceding-record-there-is-also-no-assurance-that-a-given-record-will-have-the-same-strongabsolutepositionstrong-if-the-strongrecordsetstrong-object-is-requeried-or-reopened-bookmarks-are-still-the-recommended-way-of-retaining-and-returning-to-a-given-position-and-are-the-only-way-of-positioning-across-all-types-of-strongrecordsetstrong-objectsp"></a><P>[!NOTA] La propiedad <STRONG>AbsolutePosition</STRONG> no debe utilizarse como un número de registro suplente. La posición de un registro determinado cambia al eliminar un registro anterior. Tampoco hay ninguna garantía de que un registro determinado tenga el mismo valor de <STRONG>AbsolutePosition</STRONG> si se vuelve a consultar o a abrir el objeto <STRONG>Recordset</STRONG>. Se recomienda usar marcadores para mantener y volver a una posición determinada. Además, son la única forma de establecer el posicionamiento en todos los tipos de objetos <STRONG>Recordset</STRONG>.</P>
=======
Cuando se establece la propiedad **AbsolutePosition** , incluso si se va a un registro en la memoria caché actual, ADO vuelve a cargar la memoria caché con un nuevo grupo de registros empezando por el registro que ha especificado. La propiedad [CacheSize](cachesize-property-ado.md) determina el tamaño de este grupo.


> [!NOTE]
> [!NOTA] No es aconsejable usar la propiedad **AbsolutePosition** como número de registro suplente. La posición de un registro determinado cambia cuando se elimina un registro anterior. No hay ninguna garantía de que un registro determinado tenga el mismo **AbsolutePosition** si se vuelve a consultar o se vuelve a abrir el objeto **Recordset** . Los marcadores siguen siendo la forma recomendada de conservar y volver a una posición determinada y son la única manera de ubicarse a través de todos los tipos de objetos **Recordset** .
>>>>>>> master


