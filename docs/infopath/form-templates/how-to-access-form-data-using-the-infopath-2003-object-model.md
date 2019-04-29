---
title: Obtener acceso a datos de formulario con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- xdocument interface [infopath 2007],InfoPath 2003-compatible form templates, accessing form data,XDocumentsCollection interface [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Si desea ampliar la funcionalidad de un formulario de InfoPath, con frecuencia es preciso tener acceso mediante programación a la información sobre el documento XML subyacente del formulario, tener acceso a los datos contenidos en dicho documento o realizar alguna acción en él. El modelo de objetos de InfoPath permite obtener acceso al documento XML subyacente de un formulario y manipularlo utilizando la interfaz XDocument en asociación con la interfaz XDocumentsCollection .
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416478"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Obtener acceso a datos de formulario con el modelo de objetos de InfoPath 2003

Si desea ampliar la funcionalidad de un formulario de InfoPath, con frecuencia es preciso tener acceso mediante programación a la información sobre el documento XML subyacente del formulario, tener acceso a los datos contenidos en dicho documento o realizar alguna acción en él. El modelo de objetos de InfoPath permite obtener acceso al documento XML subyacente de un formulario y manipularlo utilizando la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) en asociación con la interfaz [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
La interfaz **XDocument** es una de las más útiles del modelo de objetos de InfoPath, porque proporciona gran variedad de propiedades, métodos y eventos que no sólo interaccionan con el documento XML subyacente del formulario, sino que, además, realizan muchas de las acciones disponibles en la interfaz de usuario de InfoPath. En un proyecto de código administrado creado mediante el modelo de objetos compatible con InfoPath 2003, se define automáticamente una variable del tipo **XDocument** denominada  `thisXDocument` en el método  `_StartUp` de la clase que contiene controladores de eventos en el código de formulario del proyecto. Puede utilizar la variable  `thisXDocument` del código del formulario para obtener acceso a la interfaz **XDocument** y sus miembros. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Información general sobre la interfaz XDocumentsCollection

La interfaz **XDocumentsCollection** proporciona los siguientes métodos y propiedades que los programadores de formularios pueden utilizar para administrar los objetos **XDocument** que contiene la colección. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Cierra el formulario especificado.  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) (método)  <br/> |Crea un nuevo formulario basándose en un formulario existente.  <br/> |
|[NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx) (método)  <br/> |Crea un formulario nuevo basado en una plantilla de formulario existente.  <br/> |
|Método [NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Crea un nuevo formulario de InfoPath utilizando los datos XML y la plantilla de formulario especificados.  <br/> |
|[Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx) (método)  <br/> |Abre el formulario especificado.  <br/> |
|Propiedad [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Devuelve el número de objetos **XDocument** que contiene la colección.  <br/> |
|Propiedad [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Devuelve una referencia al objeto **XDocument** especificado.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Información general sobre la interfaz XDocument

La interfaz **XDocument** proporciona los siguientes métodos y propiedades que los programadores de formularios pueden utilizar para interactuar con el documento XML subyacente de un formulario o realizar acciones en él. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|Método [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Devuelve el valor de cadena de una variable de datos especificada.  <br/> |
|Método [GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Devuelve una referencia al modelo de objetos de documento (DOM) XML asociado al objeto **DataObject**.  <br/> |
|[ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) (método)  <br/> |Importa (o combina) el formulario especificado con el que está abierto.  <br/> |
|[PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) (método)  <br/> |Imprime la vista actual del formulario.  <br/> |
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx) (método)  <br/> |Recupera datos del adaptador de datos asociado al formulario.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Guarda el formulario abierto en ese momento.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx) Método SaveAs  <br/> |Guarda el documento abierto con el nombre indicado.  <br/> |
|Método [SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Establece el valor de una variable de datos especificada.  <br/> |
|Método [submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Envía un formulario de acuerdo con la operación de envío establecida en el modo de diseño.  <br/> |
|Propiedad [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx)  <br/> |Devuelve una referencia a la colección **DataObjects**.  <br/> |
|Propiedad [Dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Devuelve una referencia al XML DOM que se rellena con los datos XML de origen del formulario.  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) (propiedad)  <br/> |Devuelve una referencia a la colección **Errors**.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx) (propiedad)  <br/> |Devuelve una referencia a un objeto que representa todas las funciones y variables que contiene un archivo de código de formulario.  <br/> |
|[IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) (propiedad)  <br/> |Devuelve un valor **Boolean**booleano que indica si se han realizado cambios en los datos del formulario.  <br/> |
|[IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx) (propiedad)  <br/> |Devuelve un valor **Boolean**booleano que indica si el XML DOM es de sólo lectura.  <br/> |
|[IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx) (propiedad)  <br/> |Devuelve un valor **Boolean**booleano que indica si el formulario se ha guardado después de su creación  <br/> |
|[IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx) (propiedad)  <br/> |Devuelve un valor **Boolean**booleano que indica si el formulario está en modo de sólo lectura  <br/> |
|[IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) (propiedad)  <br/> |Devuelve un valor **Boolean**booleano que indica si el formulario está firmado digitalmente.  <br/> |
|[Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx) (propiedad)  <br/> |Especifica o devuelve el valor de cadena del lenguaje utilizado para el formulario.  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx) (propiedad)  <br/> |Devuelve una referencia al objeto adaptador de datos.  <br/> |
|[Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) (propiedad)  <br/> |Devuelve una referencia al objeto **Solution**.  <br/> |
|[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) (propiedad)  <br/> |Devuelve una referencia al objeto **UI**.  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx) (propiedad)  <br/> |Devuelve un valor de cadena que contiene el identificador de recursos uniforme (URI) del formulario.  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) (propiedad)  <br/> |Devuelve una referencia al objeto **View**.  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx) (propiedad)  <br/> |Devuelve una referencia a la colección **ViewInfos**.  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Uso de las interfaces XDocuments Collection y XDocument

El acceso a la interfaz **XDocumentsCollection** se obtiene a través de la propiedad [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . En los proyectos de código administrado creados con el modelo de objetos compatible con InfoPath 2003, se puede tener acceso a la interfaz **XDocumentsCollection** mediante la variable  `thisApplication`, de la que se crea una instancia en el método  `_StartUp` del código de formulario del proyecto. En el siguiente ejemplo de código, se crea una variable que hace referencia a la interfaz **XDocumentsCollection** del proyecto actual. 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

En un proyecto de código administrado creado con el modelo de objetos compatible con InfoPath 2003, se puede obtener acceso a la interfaz **XDocument** mediante la variable  `thisXDocument`, de la que se crea una instancia en el método  `StartUp` del código de formulario del proyecto. En el siguiente ejemplo de código, se utiliza la variable  `thisXDocument` para obtener acceso a la interfaz **XDocument** del proyecto para mostrar el URI del formulario que está actualmente abierto en un mensaje de alerta. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> [!NOTA] Cuando se utiliza una interfaz **XDocument** para tener acceso al documento XML subyacente de un formulario, se tiene acceso al documento XML asociado al formulario que esté abierto en ese momento. 
  
Una propiedad clave de la interfaz **XDocument** es la propiedad **DOM**. Esta propiedad devuelve una referencia al XML DOM que contiene los datos XML de origen del formulario. Cuando se utiliza la propiedad **DOM**, es posible usar cualquiera de las propiedades y los métodos admitidos por el XML DOM. Por ejemplo, en el siguiente código se utiliza la propiedad **xml** del XML DOM para mostrar todo el contenido del documento XML subyacente de un formulario: 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> [!NOTA] Para obtener más información sobre DOM XML y todas las propiedades y los métodos con los que es compatible, vea el SDK de MSXML en MSDN. 
  

