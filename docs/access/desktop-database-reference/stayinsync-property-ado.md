---
<<<<<<< Título HEAD: StayInSync (propiedad) (ADO) TOCTitle: StayInSync (propiedad) (ADO) === título: StayInSync (propiedad, ADO) TOCTitle: StayInSync (propiedad, ADO)
>>>>>>> Master ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: ms.date 48542966: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="stayinsync-property-ado"></a>StayInSync (propiedad, ADO)
=======
# <a name="stayinsync-property-ado"></a>StayInSync (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

En un objeto [Recordset](recordset-object-ado.md) jerárquico, indica si la referencia a los registros secundarios subyacentes (es decir, el *capítulo*) cambia cuando la posición de la fila superior en la jerarquía (elemento principal) cambia.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Boolean**. El valor predeterminado es **True**. Si es **True**, el capítulo se actualizará si el objeto **Recordset** primario cambia la posición de la fila; si es **False**, seguirá haciendo referencia a los datos del capítulo anterior, aun cuando el objeto **Recordset** primario haya cambiado la posición de la fila.

## <a name="remarks"></a>Comentarios

Esta propiedad se aplica a objetos Recordset jerárquicos, como los admitidos por el [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), y debe establecerse en el objeto **Recordset** primario antes de que el objeto **Recordset** secundario sea recuperado. Esta propiedad simplifica el desplazamiento por los conjuntos de registros jerárquicos.

