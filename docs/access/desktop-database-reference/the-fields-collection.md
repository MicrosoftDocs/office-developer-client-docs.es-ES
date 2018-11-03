---
title: Fields (colección)
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a73cef57a796c8791fff5bd5d9c8de1005d932f1
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945064"
---
# <a name="fields-collection"></a>Fields (colección)


**Se aplica a**: Access 2013, Office 2013

La colección **Fields** es una de las colecciones intrínsecas de ADO. Una colección es un conjunto ordenado de elementos a los que se puede hacer referencia como unidad.

La colección **Fields** contiene un objeto **Field** para cada campo (columna) del **conjunto de registros**. Igual que todas las colecciones de ADO, tiene las propiedades **Count** e **Item**, así como los métodos **Append** y **Refresh**. También tiene los métodos **CancelUpdate**, **Delete**, **Resync** y **Update**, que no están disponibles para otras colecciones de ADO.

## <a name="examining-the-fields-collection"></a>Examinar la colección Fields

Considere la colección **Fields** del **conjunto de registros** de ejemplo que se introdujo en este capítulo. El **conjunto de registros** de ejemplo se derivó de la instrucción SQL:

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Por tanto, se deberían observar tres campos en la colección **Fields** del **conjunto de registros**.

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

Este código simplemente determina el número de objetos **Field** que contiene la colección **Fields** utilizando la propiedad **Contar** y recorre en bucle la colección, para devolver el valor de la propiedad **Name** para cada objeto **Field**. Se pueden utilizar muchas más propiedades de **campo** para obtener información acerca de un campo. Para obtener más información acerca de las consultas en un **campo**, vea [El objeto Field](the-field-object.md).

## <a name="counting-columns"></a>Contar columnas

Como cabe esperar, la propiedad **Contar** devuelve la cantidad real de objetos **Field** contenidos en la colección **Fields**. Dado que la numeración de elementos de una colección empieza por cero, los bucles siempre se deben codificar a partir del elemento cero y hasta el valor de la propiedad **Contar** menos 1. Si se utiliza Microsoft Visual Basic y se desea recorrer en bucle los elementos de una colección sin comprobar la propiedad **Contar**, use el comando **For** **Each...Next**.

Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.

## <a name="getting-to-the-field"></a>Obtener el campo

Al igual que ocurre con cualquier colección de ADO, la propiedad **Item** es la predeterminada de la colección. Devuelve el objeto **Field** individual especificado por el nombre o el índice que se le pasa. Por tanto, las instrucciones siguientes son equivalentes para el **conjunto de registros** de ejemplo:

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Si estos métodos son equivalentes, ¿cuál es el mejor? Depende. El uso de un índice para recuperar un **campo** de la colección es más rápido porque obtiene acceso al **campo** directamente, sin tener que realizar una búsqueda en cadenas. Por otra parte, se debe conocer el orden de los **campos** dentro de la colección y, si cambia el orden, se tendrá que cambiar la referencia al índice del **campo** siempre que aparezca. Aunque es un método un poco más lento, el uso del nombre del **campo** es más flexible porque no depende del orden de los **campos** en la colección.

## <a name="using-the-refresh-method"></a>Utilizar el método Refresh

Al contrario que en otras colecciones de ADO, el uso del método **Refresh** con la colección **Fields** no tiene efectos visibles. Para recuperar cambios de la estructura de la base de datos subyacente, se debe usar el método **Requery** o, si el objeto **Recordset** no admite marcadores, el método **MoveFirst**, que provocará que se ejecute otra vez el comando para el proveedor.

## <a name="adding-fields-to-a-recordset"></a>Agregar campos a un conjunto de registros

El método **Append** se utiliza para agregar campos a un **conjunto de registros**.

El método **Append** se puede utilizar para fabricar un **conjunto de registros** mediante programación sin abrir una conexión con un origen de datos. Si se llama al método **Append** en la colección **Fields** de un **conjunto de registros** abierto o en un **conjunto de registros** donde se ha configurado la propiedad **ActiveConnection**, se producirá un error en tiempo de ejecución. Sólo se pueden anexar campos a un **conjunto de registros** que no esté abierto y que aún no se haya conectado a un origen de datos. No obstante, para especificar valores para los **campos** recién anexados, primero se debe abrir el **conjunto de registros**.

Con frecuencia, los programadores necesitan una ubicación para almacenar temporalmente algunos datos, o desean que ciertos datos se comporten como si procediesen de un servidor, para que puedan participar en enlaces de datos en una interfaz de usuario. ADO (junto con el [servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permite al programador crear un objeto **Recordset** vacío especificando información de columnas y llamando a **Open**. En el siguiente ejemplo, se anexan tres nuevos campos a un nuevo objeto **Recordset**. A continuación, se abre el **conjunto de registros**, se agregan dos nuevos registros y se conserva el **conjunto de registros** en un archivo (para obtener más información acerca de la persistencia de **conjuntos de registros**, vea el [Capítulo 5: Actualizar y almacenar datos](chapter-5-updating-and-persisting-data.md)).

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

El uso del método **Append** de **Fields** difiere entre el objeto **Recordset** y el objeto **Record**. Para obtener más información acerca del objeto **Record**, vea el [Capítulo 10: Objetos Record y Stream](chapter-10-records-and-streams.md).

