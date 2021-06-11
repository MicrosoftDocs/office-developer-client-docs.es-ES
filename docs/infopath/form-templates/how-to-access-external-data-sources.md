---
title: Obtener acceso a orígenes de datos externos
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- data connection classes [infopath 2007],secondary data sources [InfoPath 2007],data [InfoPath 2007], secondary,DataSource class [InfoPath 2007],accessing external data sources [InfoPath 2007],DataSourceCollection class [InfoPath 2007],DataConnectionCollection class [InfoPath 2007],DataConnection class [InfoPath 2007],InfoPath 2007, accessing external data,data [InfoPath 2007], external sources
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Al trabajar con una plantilla de formulario de InfoPath, puede escribir código para obtener acceso a los orígenes de datos secundarios y manipular los datos que contienen.
ms.openlocfilehash: f6957c561231eef0e3e4df6deb09ae89f85afcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408316"
---
# <a name="access-external-data-sources"></a>Obtener acceso a orígenes de datos externos

Al trabajar con una plantilla de formulario de InfoPath, puede escribir código para obtener acceso a los orígenes de datos secundarios y manipular los datos que contienen. 
  
Cada origen de datos secundario está representado mediante un objeto del que se crea una instancia utilizando la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) y que corresponde a datos almacenados obtenidos de algún origen de datos externos, como una base de datos o una consulta de servicio Web. Estos orígenes de datos se denominan secundarios porque cuando el usuario guarda un formulario de InfoPath, sólo guarda los datos del origen de datos principal (o primario), no los de los orígenes de datos secundarios. La conexión a un origen de datos se representa mediante un objeto del que se crea una instancia utilizando una de las clases de "adaptador de datos", como la clase [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , que representa una conexión de datos a un servicio Web XML. 
  
El objeto del que se crea una instancia [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) representa el almacenamiento de datos XML que devuelve una conexión de datos (de una base de datos o a una consulta de servicio web) y la clase de "conexión de datos" representa la propia conexión de datos (como se define y denomina usando el comando **Conexiones de datos** de la ficha **Datos**). 
  
El modelo de objetos de InfoPath admite el acceso a los orígenes de datos secundarios de un formulario mediante la utilización de la clase [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) en asociación con la clase [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) . 
  
El modelo de objetos de InfoPath también proporciona un conjunto de clases de conexión de datos que contienen información sobre las conexiones de datos que utiliza el formulario.
  
> [!NOTE]
> [!NOTA] En Microsoft InfoPath 2003, una conexión de datos se denomina adaptador de datos. 
  
Los adaptadores de datos pueden ser de dos tipos: conexiones de consultas, que se utilizan para obtener datos que después se almacenan en un origen de datos secundario y conexiones de envío que se utilizan para enviar datos, por ejemplo a una base de datos o a un servicio web. Los datos enviados se copian de orígenes de datos principales o secundarios. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Información general sobre la clase DataSourceCollection

La clase [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) proporciona las siguientes propiedades y métodos que los programadores de formularios pueden utilizar para administrar las instancias de [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) que contenga el formulario. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Devuelve el número de instancias de objetos **DataSource** contenidas en la colección.  <br/> |
|[GetEnumerator (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Devuelve un **IEnumerator** que se puede utilizar para recorrer en iteración la colección.  <br/> |
|[Propiedad Item[Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Devuelve una referencia al objeto **DataSource** especificado de la colección por su valor de índice.  <br/> |
|[Propiedad Item[String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Devuelve una referencia al objeto **DataSource** especificado por nombre.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Información general sobre la clase DataSource

La clase [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) proporciona el método y las propiedades siguientes que los programadores de formularios pueden utilizar para interactuar con un origen de datos secundario de InfoPath. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[CreateNavigator (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Devuelve un [objeto XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para obtener acceso al origen de datos y editarlo.  <br/> |
|[QueryConnection (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Obtiene una referencia al objeto de conexión de datos asociado.  <br/> Para ejecutar la consulta en la conexión de datos e insertar los datos devueltos como XML en el nodo XML asociado al **objeto DataSource,** use el método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) del objeto de conexión de datos asociado.  <br/> |
|Propiedad [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Obtiene el nombre del objeto **DataSource**.  <br/> |
|[ReadOnly (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Obtiene un valor que indica si el origen de datos está en un estado de sólo lectura.  <br/> |
|[GetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Obtiene el valor de una propiedad con nombre para el nodo XML especificado, que debe ser un nodo **nonattribute** en el origen de datos principal.  <br/> |
|[SetNamedNodeProperty (método)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Establece el valor de una propiedad con nombre para el nodo XML especificado, que deberá ser un nodo **nonattribute** en el origen de datos principal.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Información general sobre las clases de conexión de datos

Las clases para obtener acceso a conexiones de datos ofrecen distintas propiedades y métodos que recuperan y envían datos a través de conexiones a orígenes de datos externos. La conexión de datos que se asocie a un objeto **DataSource** dependerá del tipo de conexión de datos externos que se utilice. InfoPath implementa las siguientes clases para obtener acceso a conexiones de datos. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[Clase AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Consulta un origen de datos ADO/OLEDB (sólo en Microsoft Access y Microsoft SQL Server).  <br/> |
|[Clase AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Envía un origen de datos ADO/OLEDB (sólo en Microsoft Access y Microsoft SQL Server).  <br/> |
|[Clase SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Consulta una biblioteca de documentos o lista de SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Se conecta a una biblioteca de documentos o una lista de SharePoint.  <br/> |
|[Clase WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Se conecta a un servicio Web XML.  <br/> |
|[Clase FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Consulta un archivo XML.  <br/> |
|[Clase FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Envía un archivo XML.  <br/> |
|[Clase EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Envía un formulario como datos adjuntos en el correo electrónico.  <br/> |
|[Clase BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Consulta una lista externa en un servidor que ejecuta SharePoint Foundation 2010 o SharePoint Server 2010.  <br/> |
|[Clase BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Se envía a una lista externa en un servidor que ejecuta SharePoint Foundation 2010 o SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Uso de las clases DataSourceCollection DataSource

Se tiene acceso al objeto **DataSourceCollection** que representa la colección de orígenes de datos asociada con una plantilla de formulario a través de la propiedad [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Por ejemplo, si se crea un origen de datos secundario denominado Empleados que recupera datos de la tabla Empleados de la base de datos Neptuno, puede usar el objeto **DataSourceCollection** para establecer una referencia al objeto **DataSource** que representa los datos recuperados. 
  
En el ejemplo de código siguiente, el nombre del origen de datos secundarios se pasa a la propiedad descriptor de acceso de la clase **DataSourceCollection**, que devuelve una referencia al objeto **DataSource** que representa los datos de la tabla Empleados recuperados. En nodo XML que almacena los datos recuperados del origen de datos secundario se muestra en un cuadro de diálogo usando el método **CreateNavigator** de la clase **DataSource** para tener acceso a la propiedad **InnerXml** de la clase **XPathNavigator**. 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

Para manipular los datos contenidos en un origen de datos secundario, utilice el método **CreateNavigator** de la clase **DataSource** para devolver una referencia a un objeto **XPathNavigator** situado en el nodo en el que se almacenan los datos secundarios. Puede usar las propiedades o los métodos de la clase **XPathNavigator** para manipular los datos. Para obtener más información, [vea Trabajar con las clases XPathNavigator y XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Uso de las clases DataSourceCollection y DataConnection

El objeto [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) que representa las conexiones de datos asociadas con una plantilla de formulario a través de la propiedad [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) de la clase **XmlForm**. Por ejemplo, si crea un origen de datos secundario llamado Empleados que recupera datos de la tabla Empleados de la base de datos Neptuno, puede usar el objeto **DataConnectionCollection** asociado a la plantilla de formulario para establecer una referencia a la **DataConnection** que representa la conexión con la base de datos. 
  
En el siguiente ejemplo de código, el nombre del origen de datos secundario se pasa a la propiedad descriptor de acceso de la clase **DataConnectionCollection**, que en este caso devuelve una referencia al objeto **ADOQueryConnection** que representa la conexión a la base de datos Neptuno. Para que esto funcione correctamente, debe convertir explícitamente el objeto devuelto en tipo **ADOQueryConnection**. La propiedad [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) de la interfaz **ADOAdapterObject** se utiliza para mostrar la cadena de conexión ADO en un cuadro de mensaje. 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>Vea también



[Crear plantillas de formulario de InfoPath que funcionan con InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

