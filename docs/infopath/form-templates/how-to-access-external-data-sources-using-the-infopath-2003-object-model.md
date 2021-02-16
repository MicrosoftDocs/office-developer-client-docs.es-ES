---
title: Obtener acceso a orígenes de datos externos mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- data sources [infopath 2007], accessing with infopath 2003 object model,InfoPath 2003-compatible form templates, accessing external data
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Al trabajar con una plantilla de formulario de InfoPath que use el modelo de objetos compatible con InfoPath 2003, puede escribir código para obtener acceso a los orígenes de datos secundarios del formulario y manipular los datos que contienen.
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431683"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Obtener acceso a orígenes de datos externos mediante el modelo de objetos de InfoPath 2003

Al trabajar con una plantilla de formulario de InfoPath que use el modelo de objetos compatible con InfoPath 2003, puede escribir código para obtener acceso a los orígenes de datos secundarios del formulario y manipular los datos que contienen.
  
Cada origen de datos secundario está representado por un objeto del que se crea una instancia utilizando la interfaz [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) y que corresponde a datos almacenados obtenidos de algún origen de datos externos, como una base de datos o una consulta de servicio web. Estos orígenes de datos se denominan secundarios porque cuando el usuario guarda un formulario de InfoPath, sólo guarda los datos del origen de datos principal, no los de los orígenes de datos secundarios. La conexión a un origen de datos se representa mediante un objeto del que se crea una instancia utilizando una de las interfaces "adaptador de datos", como la interfaz [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) , que representa una conexión de datos a un servicio Web XML. 
  
El objeto [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) del que se crea una instancia representa el almacenamiento de datos XML que devuelve una conexión de datos (a una base de datos o a una consulta de servicio web); el adaptador de datos representa la propia conexión de datos. 
  
El modelo de objetos de InfoPath admite el acceso a los orígenes de datos secundarios de un formulario mediante la utilización de la interfaz [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) en asociación con la interfaz [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) . 
  
El modelo de objetos de InfoPath también proporciona un conjunto de objetos de adaptador de datos que contienen información sobre las conexiones de datos que utiliza el formulario. 
  
Hay dos tipos de adaptadores de datos: adaptadores de datos y adaptadores de envío. Los adaptadores de consulta se usan para obtener los datos que, a continuación, se almacenan en un origen de datos secundario, mientras que los adaptadores de envío se usan para enviar datos, por ejemplo a una base de datos o a un servicio web. Los datos enviados se copian de los orígenes de datos principal o secundario. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Información general sobre la interfaz DataObjectsCollection

La interfaz [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) proporciona las siguientes propiedades y métodos que los programadores de formularios pueden utilizar para administrar las instancias de [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) que contenga el formulario. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Devuelve el número de instancias **DataSourceObject** contenidas en la colección  <br/> |
|[Método GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Devuelve un **IEnumerator** que se puede utilizar para recorrer en iteración la colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Devuelve una referencia a la instancia **DataSourceObject** especificada  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Información general sobre la interfaz DataSourceObject

La interfaz [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) proporciona el método y las propiedades siguientes que los programadores de formularios pueden utilizar para interactuar con un origen de datos secundario de InfoPath. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[Método de](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) consulta  <br/> |Ejecuta la consulta en el adaptador de datos e inserta los datos devueltos como XML en el modelo de objetos de documento (DOM) XML asociado a **DataSourceObject**.  <br/> |
|[Dom (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Devuelve una referencia al XML DOM que se utiliza para almacenar y manipular datos mediante **DataSourceObject**.  <br/> |
|Propiedad [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Devuelve un valor de cadena que indica el nombre de **DataSourceObject**  <br/> |
|[QueryAdapter (propiedad)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Devuelve una referencia al objeto adaptador de datos asociado.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Información general sobre las interfaces de adaptadores de datos

Las interfaces para obtener acceso a adaptadores de datos ofrecen distintas propiedades y métodos que recuperan y envían datos a través de conexiones a orígenes de datos externos. El adaptador de datos que se asocie a un objeto [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) dependerá del tipo de conexión de datos externos que se utilice. InfoPath implementa las siguientes interfaces para obtener acceso a adaptadores de datos: 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[Interfaz ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Se conecta a orígenes de datos ADO/OLEDB (sólo en Microsoft Access y Microsoft SQL Server™).  <br/> |
|[Interfaz SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Se conecta a una biblioteca de documentos o lista de SharePoint.  <br/> |
|[Interfaz WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Se conecta a servicios web XML.  <br/> |
|[XMLFileAdapterObject (objeto)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Se conecta a un archivo XML.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Uso de las interfaces DataSourceObjects y DataSourceObject

El acceso a la colección **DataSourceObjects** se obtiene a través de la propiedad [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Por ejemplo, si crea un origen de datos secundario con el nombre Empleados que recupera datos de la tabla Empleados de la base de datos Neptuno de Microsoft Access, puede utilizar la colección **DataSourceObjects** para establecer una referencia al objeto **DataObject** que representa los datos recuperados. 
  
En el ejemplo de código siguiente, el nombre del origen de datos secundarios se pasa a la propiedad de descriptor de acceso de la interfaz **DataObjectsCollection**, que devuelve una referencia al objeto **DataSourceObject**. Los datos del origen de datos secundario se muestran en un cuadro de mensaje mediante la propiedad **DOM** de la interfaz **DataSourceObject** para obtener acceso a la propiedad **xml** del XML DOM. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

Para manipular los datos contenidos en un origen de datos secundario, utilice la propiedad **DOM** de la interfaz **DataSourceObject** para devolver una referencia al XML DOM que contiene los datos. Si se tiene la referencia al XML DOM, se puede usar cualquiera de sus propiedades o métodos para manipular los datos que contiene. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Uso de las interfaces DataAdaptersCollection y DataAdapterObject

El acceso a la interfaz [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) se obtiene a través de la propiedad [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) de la interfaz **XDocument**. Por ejemplo, si crea un origen de datos secundario con el nombre Empleados que recupera datos de la tabla Empleados de la base de datos Neptuno de Microsoft Access, puede utilizar la colección **DataAdapterObjects** para establecer una referencia al objeto **DataAdapterObject** que representa la conexión a la base de datos. 
  
En el siguiente ejemplo de código, el nombre del origen de datos secundario se pasa a la propiedad de descriptor de acceso de la colección **DataAdaptersCollection**, que en este caso devuelve una referencia a una instancia del objeto **ADOAdapterObject** que representa la conexión a la base de datos Neptuno de Microsoft Access. Para que esto funcione correctamente, debe convertir explícitamente el objeto devuelto en objeto **ADOAdapterObject**. La propiedad [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) de la interfaz **ADOAdapterObject** se utiliza para mostrar la cadena de conexión ADO en un cuadro de mensaje. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


