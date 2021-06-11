---
title: Trabajar con firmas digitales con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007], infopath 2003-compatible form templates,InfoPath 2003-compatible form templates, digital signatures
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: El modelo de objetos compatible con InfoPath 2003 proporciona características para trabajar con firmas digitales mediante programación.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433447"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a><span data-ttu-id="40244-104">Trabajar con firmas digitales con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="40244-104">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="40244-105">El modelo de objetos compatible con InfoPath 2003 proporciona características para trabajar con firmas digitales mediante programación.</span><span class="sxs-lookup"><span data-stu-id="40244-105">The InfoPath 2003-compatible object model provides features for working with digital signatures programmatically.</span></span>
  
## <a name="digital-signature-features"></a><span data-ttu-id="40244-106">Características de las firmas digitales</span><span class="sxs-lookup"><span data-stu-id="40244-106">Digital Signature Features</span></span>

<span data-ttu-id="40244-107">Las características de firmas digitales disponibles en InfoPath permiten:</span><span class="sxs-lookup"><span data-stu-id="40244-107">The digital signatures features available in InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="40244-108">Habilitar las firmas para todo el formulario o para conjuntos específicos de datos del formulario que se puedan firmar por separado.</span><span class="sxs-lookup"><span data-stu-id="40244-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="40244-p101">Especificar, por cada conjunto de datos que se pueda firmar, si se permiten una o varias firmas y la relación que tendrán. Por ejemplo, puede indicar si son cofirmas en paralelo o si cada nueva firma contrafirma todas las anteriores.</span><span class="sxs-lookup"><span data-stu-id="40244-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="40244-111">Especificar un mensaje que se va a mostrar a los usuarios del formulario cuando lo firmen.</span><span class="sxs-lookup"><span data-stu-id="40244-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="40244-112">Insertar y ver una firma en el documento.</span><span class="sxs-lookup"><span data-stu-id="40244-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="40244-p102">Ver la información de no incumplimiento comprobable que se ha añadido a cada firma para incrementar la seguridad. Esta información adicional, que incluye una vista del formulario tal como se ha presentado a cada firmante, es una parte de la firma y no se puede quitar sin invalidar ésta. En cualquier momento, puede recuperar estos datos haciendo clic en la firma del formulario para mostrar el cuadro de diálogo **Comprobar firma digital**.</span><span class="sxs-lookup"><span data-stu-id="40244-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="40244-p103">Sacar partido de un modelo de objetos para trabajar con firmas digitales. Añadir información personalizada al bloque de la firma de los formularios de plena confianza mediante el modelo de objetos de firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="40244-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="40244-118">Información general sobre el modelo de objetos de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="40244-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="events"></a><span data-ttu-id="40244-119">Eventos</span><span class="sxs-lookup"><span data-stu-id="40244-119">Events</span></span>

<span data-ttu-id="40244-120">El modelo de objetos de firmas digitales proporciona el siguiente evento.</span><span class="sxs-lookup"><span data-stu-id="40244-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="40244-121">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40244-121">**Name**</span></span>|<span data-ttu-id="40244-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40244-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40244-123">OnSign</span><span class="sxs-lookup"><span data-stu-id="40244-123">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="40244-124">Se produce después de seleccionar un conjunto de datos para firmarlos.</span><span class="sxs-lookup"><span data-stu-id="40244-124">Occurs after a set of signable data has been selected to sign.</span></span>  <br/> <span data-ttu-id="40244-p104">Puede utilizar este evento para manipular los datos almacenados en la firma digital. Por ejemplo, se pueden agregar datos de un servidor de marca de tiempo de confianza o agregar una contrafirma del lado servidor de la transacción. Asimismo, se puede usar este evento para bloquear la firma si el usuario actual no es integrante de un grupo determinado.</span><span class="sxs-lookup"><span data-stu-id="40244-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
<span data-ttu-id="40244-128">El evento **OnSign** devuelve una referencia al objeto [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , que proporciona las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="40244-128">The **OnSign** event returns a reference to the [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="40244-129">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40244-129">**Name**</span></span>|<span data-ttu-id="40244-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40244-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40244-131">ReturnStatus</span><span class="sxs-lookup"><span data-stu-id="40244-131">ReturnStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |<span data-ttu-id="40244-132">Obtiene o establece un valor **Boolean** que indica el estado de retorno del evento **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="40244-132">Gets or sets a **Boolean** value indicating the return status of the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="40244-133">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="40244-133">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |<span data-ttu-id="40244-134">Obtiene el bloque de datos firmados que desencadenó el evento **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="40244-134">Gets the signed data block that triggered the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="40244-135">XDocument</span><span class="sxs-lookup"><span data-stu-id="40244-135">XDocument</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |<span data-ttu-id="40244-136">Obtiene una referencia al objeto **XDocument** asociado al evento **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="40244-136">Gets a reference to the **XDocument** object associated with the **OnSign** event.</span></span>  <br/> |
   
### <a name="collections-and-objects"></a><span data-ttu-id="40244-137">Colecciones y objetos</span><span class="sxs-lookup"><span data-stu-id="40244-137">Collections and Objects</span></span>

<span data-ttu-id="40244-138">El modelo de objetos de firmas digitales proporciona las siguientes colecciones.</span><span class="sxs-lookup"><span data-stu-id="40244-138">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="40244-139">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40244-139">**Name**</span></span>|<span data-ttu-id="40244-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40244-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40244-141">SignedDataBlocksCollection</span><span class="sxs-lookup"><span data-stu-id="40244-141">SignedDataBlocksCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |<span data-ttu-id="40244-142">La colección de los [objetos SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) de la plantilla de formulario tal como se define en el archivo de definición de formulario (.xsf).</span><span class="sxs-lookup"><span data-stu-id="40244-142">The collection of the [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) objects in the form template as defined in the form definition file (.xsf).</span></span>  <br/> <span data-ttu-id="40244-143">La colección **SignedDataBlocksCollection** implementa propiedades que se pueden usar para obtener acceso a los objetos **SignedDataBlockObjects** asociados con un formulario.</span><span class="sxs-lookup"><span data-stu-id="40244-143">The **SignedDataBlocksCollection** collection implements properties that can be used to access the **SignedDataBlockObjects** objects associated with a form.</span></span> <span data-ttu-id="40244-144">Se puede acceder a la colección **SignedDataBlocks** a través de la [propiedad SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) del [objeto XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)</span><span class="sxs-lookup"><span data-stu-id="40244-144">The **SignedDataBlocks** collection is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) object.</span></span>  <br/> |
|[<span data-ttu-id="40244-145">SignaturesCollection</span><span class="sxs-lookup"><span data-stu-id="40244-145">SignaturesCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |<span data-ttu-id="40244-146">Contiene una colección de [objetos SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) para cada **SignedDataBlockObject** en el formulario.</span><span class="sxs-lookup"><span data-stu-id="40244-146">Contains a collection of [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objects for each **SignedDataBlockObject** in the form.</span></span>  <br/> <span data-ttu-id="40244-p106">La colección **SignaturesCollection** implementa propiedades y un método que se pueden usar para obtener acceso a objetos **SignatureObject** asociados con el formulario y crear una firma. Se puede obtener acceso a esta colección mediante el objeto **SignedDataBlockObject**.</span><span class="sxs-lookup"><span data-stu-id="40244-p106">The **SignaturesCollection** collection implements properties and a method that can be used to access a form's associated **SignatureObject** objects and to create a signature. It is accessible through the **SignedDataBlockObject** object.  </span></span><br/> <span data-ttu-id="40244-149">Cuando use el [método Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) de la colección **SignaturesCollection,** tenga en cuenta que la firma no se escribe hasta que se llame al método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) en el **objeto SignatureObject.**</span><span class="sxs-lookup"><span data-stu-id="40244-149">When you use the [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) method of the **SignaturesCollection** collection, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method is called on the **SignatureObject** object.</span></span> <span data-ttu-id="40244-150">Sólo se pueden llamar estos métodos desde el controlador de eventos **OnSign** de una plantilla de formulario de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="40244-150">These methods can be called only from the **OnSign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="40244-151">El modelo de objetos de firmas digitales proporciona los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="40244-151">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="40244-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40244-152">**Name**</span></span>|<span data-ttu-id="40244-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40244-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40244-154">SignedDataBlockObject</span><span class="sxs-lookup"><span data-stu-id="40244-154">SignedDataBlockObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |<span data-ttu-id="40244-p108">Representa un conjunto de datos que se pueden firmar en un formulario. El objeto **SignedDataBlock** proporciona una serie de propiedades y un método que se pueden usar para interactuar mediante programación con un conjunto de datos que se pueden firmar.</span><span class="sxs-lookup"><span data-stu-id="40244-p108">Represents a set of signable data in a form. The **SignedDataBlock** object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.  </span></span><br/> |
|[<span data-ttu-id="40244-157">SignatureObject</span><span class="sxs-lookup"><span data-stu-id="40244-157">SignatureObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |<span data-ttu-id="40244-158">Representa una firma digital agregada a un formulario o a un conjunto de datos que se pueden firmar de un formulario.</span><span class="sxs-lookup"><span data-stu-id="40244-158">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="40244-159">La **colección SignatureObject** implementa propiedades que se pueden usar para recuperar información sobre la firma digital y el método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) para escribir el bloque de firma digital XML e calcular su valor hash criptográfico.</span><span class="sxs-lookup"><span data-stu-id="40244-159">The **SignatureObject** collection implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="40244-160">CertificateObject</span><span class="sxs-lookup"><span data-stu-id="40244-160">CertificateObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |<span data-ttu-id="40244-161">Representa el certificado digital X.509 utilizado para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="40244-161">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="40244-162">Trabajar con firmas digitales mediante programación</span><span class="sxs-lookup"><span data-stu-id="40244-162">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="40244-p110">El modelo de objetos compatible con InfoPath 2003 ofrece miembros para interactuar con las firmas digitales mediante programación. Concretamente, los formularios de plena confianza pueden añadir información personalizada al bloque de la firma antes de confirmarlo, de acuerdo con la siguiente escala de tiempo:</span><span class="sxs-lookup"><span data-stu-id="40244-p110">The InfoPath 2003-compatible object model provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span>
  
1. <span data-ttu-id="40244-165">El usuario elige agregar una firma digital a un formulario.</span><span class="sxs-lookup"><span data-stu-id="40244-165">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="40244-166">Se muestra el primer panel del **Asistente para firmas digitales**.</span><span class="sxs-lookup"><span data-stu-id="40244-166">The first panel of the **Digital Signature Wizard** is displayed.</span></span> 
    
3. <span data-ttu-id="40244-167">Se inicia el evento **OnSign** de los datos seleccionados que representa el objeto **SignedDataBlockObject** y se ejecutan el método **Sign** de **SignedDataBlockObject** y el método **Create** de **SignaturesCollection**.</span><span class="sxs-lookup"><span data-stu-id="40244-167">The **OnSign** event for the selected data represented by the **SignedDataBlockObject** object is raised, and the **Sign** method of **SignedDataBlockObject** and the **Create** method of the **SignaturesCollection** collection are executed.</span></span> 
    
4. <span data-ttu-id="40244-168">Se ejecutan todas las acciones personalizadas opcionales.</span><span class="sxs-lookup"><span data-stu-id="40244-168">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="40244-169">Se ejecuta el método **Sign** de **SignatureObject**.</span><span class="sxs-lookup"><span data-stu-id="40244-169">The **Sign** method of the **SignatureObject** is executed.</span></span> 
    
6. <span data-ttu-id="40244-170">Se muestran el segundo y el tercer panel del asistente para seleccionar el certificado de la firma y escribir comentarios.</span><span class="sxs-lookup"><span data-stu-id="40244-170">Second and third panes of the wizard are displayed for selecting a certificate to sign with and to enter comments.</span></span>
    
7. <span data-ttu-id="40244-171">Se muestra la información de no incumplimiento (que se puede ver más tarde con el cuadro de diálogo **Comprobar firma digital**).</span><span class="sxs-lookup"><span data-stu-id="40244-171">The non-repudiation information is displayed (which can be viewed later with the **Verify Digital Signature** dialog box).</span></span> 
    
8. <span data-ttu-id="40244-172">Al hacer clic en el botón **Firmar**, se agrega la firma a la colección de firmas del formulario.</span><span class="sxs-lookup"><span data-stu-id="40244-172">When the **Sign** button is clicked, the signature is added to collection of signatures for the form.</span></span> 
    
<span data-ttu-id="40244-173">En el ejemplo siguiente, se invoca el cuadro de diálogo **Firmar** y se contrafirma la firma con un valor de marca de tiempo recuperado de un servicio de marca de tiempo de confianza.</span><span class="sxs-lookup"><span data-stu-id="40244-173">The following example invokes the **Sign** dialog box and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


