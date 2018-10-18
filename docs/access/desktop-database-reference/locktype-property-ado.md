---
<<<<<<< Título HEAD: propiedad LockType (ADO) TOCTitle: propiedad LockType (ADO) === título: LockType (propiedad, ADO) TOCTitle: LockType (propiedad, ADO)
>>>>>>> Master ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: ms.date 48543589: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="locktype-property-ado"></a>LockType (propiedad, ADO)
=======
# <a name="locktype-property-ado"></a>LockType (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el tipo de bloqueos colocados en registros durante la modificación.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo [LockTypeEnum](locktypeenum.md). El valor predeterminado es **adLockReadOnly**.

## <a name="remarks"></a>Comentarios

Establezca la propiedad **LockType** antes de abrir un objeto [Recordset](recordset-object-ado.md) a fin de especificar el tipo de bloqueo que el proveedor debe usar al abrirlo. Lea la propiedad para devolver el tipo de bloqueo en uso a un objeto **Recordset**.

Es posible que los proveedores no admitan todos los tipos de bloqueo. Si un proveedor no puede admitir el valor **LockType** solicitado, lo sustituirá por otro tipo de bloqueo. Para determinar la funcionalidad de bloqueo real disponible en un objeto **Recordset**, use el método [Supports](supports-method-ado.md) con **adUpdate** y **adUpdateBatch**.

No se admite el valor **adLockPessimistic** cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**. Si se establece un valor no admitido, no se producirá ningún error; se utilizará el valor admitido de **LockType** más cercano.

La propiedad **LockType** es de lectura y escritura cuando el objeto **Recordset** está cerrado y de sólo lectura cuando está abierto.

**Uso de servicio de datos remotos** Cuando se usa en un objeto Recordset de cliente, sólo puede establecerse la propiedad **LockType** en **adLockBatchOptimistic**.

