---
<<<<<<< Título HEAD: PageCount (propiedad) (ADO) TOCTitle: PageCount (propiedad) (ADO) === título: PageCount (propiedad, ADO) TOCTitle: PageCount (propiedad, ADO)
>>>>>>> Master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: ms.date 48546609: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="pagecount-property-ado"></a>PageCount (propiedad, ADO)
=======
# <a name="pagecount-property-ado"></a>PageCount (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica cuántas páginas de datos contiene el objeto [Recordset](recordset-object-ado.md).

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **Long** que indica el número de páginas del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**. *Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad [PageSize](pagesize-property-ado.md) . Aunque la última página esté incompleta debido a que existan menos registros que el valor **PageSize**, cuenta como una página adicional en el valor **NúmeroDePáginas (PageCount)**. Si el objeto **Recordset** no admite esta propiedad, el valor será -1 para indicar que **NúmeroDePáginas (PageCount)** es indeterminable.

Vea las propiedades **PageSize** y [AbsolutePage](absolutepage-property-ado.md) para obtener más información acerca de la funcionalidad de las páginas.

