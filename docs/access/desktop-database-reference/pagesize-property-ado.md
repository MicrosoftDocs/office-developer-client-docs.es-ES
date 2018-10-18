---
<<<<<<< Título HEAD: PageSize (propiedad) (ADO) TOCTitle: PageSize (propiedad) (ADO) === título: PageSize (propiedad, ADO) TOCTitle: PageSize (propiedad, ADO)
>>>>>>> Master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: ms.date 48548079: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="pagesize-property-ado"></a>PageSize (propiedad, ADO)
=======
# <a name="pagesize-property-ado"></a>PageSize (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica cuántos registros constituyen una página en el objeto [Recordset](recordset-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve un valor de tipo **Long** que indica cuántos registros hay en una página. El valor predeterminado es 10.

## <a name="remarks"></a>Comentarios

<<<<<<< HEAD utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.
=== Utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad [AbsolutePage](absolutepage-property-ado.md) para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor web cuando desea permitir al usuario desplazarse por los datos, ve un cierto número de registros a la vez.
>>>>>>> master

Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.

