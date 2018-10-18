---
<<<<<<< Título HEAD: AbsolutePage (propiedad) (ADO) TOCTitle: AbsolutePage (propiedad) (ADO) ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: ms.date 48547288: 18/09/2015 mtps_version: v = Office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage (propiedad, ADO)

=== título: AbsolutePage (propiedad, ADO) TOCTitle: AbsolutePage (propiedad, ADO) ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: ms.date 48547288: 17/10/2018 mtps_version: Office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage (propiedad, ADO)
>>>>>>> master

**Se aplica a**: Access 2013 | Office 2013

Indica en qué página reside el registro actual.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos

<a name="sets-or-returns-a-long-value-from-1-to-the-number-of-pages-in-the-recordsetrecordset-object-adomd-object--pagecountpagecount-property-adomd--or-returns-one-of-the-positionenumpositionenummd-values"></a>Establece o devuelve un valor de tipo **Long** comprendido entre 1 y el número de páginas del objeto [Recordset](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md).
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de **tipo Long** entre 1 y el número de páginas en el objeto [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) o bien, devuelve uno de los valores de [PositionEnum](positionenum.md) .
>>>>>>> master

## <a name="remarks"></a>Comentarios

Esta propiedad puede usarse para identificar el número de página donde está ubicado el registro actual. Usa la propiedad [PageSize](pagesize-property-ado.md) para dividir lógicamente el número total de conjuntos de filas del objeto **Recordset** en series de páginas, cada una con un número de registros equivalente a **PageSize** (salvo en el caso de la última página, que puede tener menos registros). El proveedor debe admitir la funcionalidad apropiada para que esta propiedad esté disponible.

Al obtener o establecer la propiedad **AbsolutePage**, ADO usa la propiedad [AbsolutePosition](absoluteposition-property-ado.md) y la propiedad [PageSize](pagesize-property-ado.md) conjuntamente de la siguiente manera:

<<<<<<< HEAD
  - Para obtener el valor de **AbsolutePage**, ADO recupera primero el valor de **AbsolutePosition** y, a continuación, lo divide entre el valor de **PageSize**.

  - Para establecer el valor de **AbsolutePage**, ADO mueve **AbsolutePosition** de la siguiente forma: multiplica el valor de **PageSize** por el nuevo valor de **AbsolutePage** y, a continuación, le suma 1. Como resultado, la posición actual en el objeto **Recordset** después de establecer correctamente el valor de **AbsolutePage** es el primer registro de esa página.
=======
- Para obtener el valor de **AbsolutePage**, ADO recupera primero el valor de **AbsolutePosition** y, a continuación, lo divide entre el valor de **PageSize**.

- Para establecer el valor de **AbsolutePage**, ADO mueve **AbsolutePosition** de la siguiente forma: multiplica el valor de **PageSize** por el nuevo valor de **AbsolutePage** y, a continuación, le suma 1. Como resultado, la posición actual en el **objeto Recordset** después de establecer correctamente el valor de **AbsolutePage** es el primer registro de esa página.
>>>>>>> master

Al igual que la propiedad **AbsolutePosition**, **AbsolutePage** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Establezca esta propiedad para desplazarse al primer registro de una página determinada. Obtenga el número total de páginas de la propiedad **PageCount**.

