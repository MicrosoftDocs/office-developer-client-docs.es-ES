---
<<<<<<< Título HEAD: SQLState (propiedad) (ADO) TOCTitle: SQLState (propiedad) (ADO) === título: SQLState (propiedad, ADO) TOCTitle: SQLState (propiedad, ADO)
>>>>>>> Master ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: ms.date 48547806: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="sqlstate-property-ado"></a>SQLState (propiedad, ADO)
=======
# <a name="sqlstate-property-ado"></a>SQLState (propiedad, ADO)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Indica el estado SQL de un objeto [Error](error-object-ado.md) especificado.

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de cinco caracteres de tipo **String** que sigue el estándar ANSI SQL e indica el código del error.

## <a name="remarks"></a>Comentarios

Use la propiedad **SQLState** para leer el código de error de cinco caracteres que devuelve el proveedor cuando se produce un error durante el procesamiento de una instrucción SQL. Por ejemplo, cuando se usa el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error de estado SQL se originan en ODBC, basándose en errores específicos de ODBC o en errores que se originan en Microsoft SQL Server, y se asignan a errores ODBC. Estos códigos de error están documentados en el estándar ANSI de SQL, pero pueden ser implementados de formas diferentes por los distintos orígenes de datos.

