---
title: Trabajar con firmas digitales
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007],InfoPath 2007, digital signatures
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: El modelo de objetos del espacio de nombres Microsoft.Office.InfoPath ofrece características para trabajar con firmas digitales mediante programación.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425578"
---
# <a name="work-with-digital-signatures"></a><span data-ttu-id="b1f3a-104">Trabajar con firmas digitales</span><span class="sxs-lookup"><span data-stu-id="b1f3a-104">Work with Digital Signatures</span></span>

<span data-ttu-id="b1f3a-105">El modelo de objetos del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) ofrece características para trabajar con firmas digitales mediante programación.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-105">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides features for working with digital signatures programmatically.</span></span> 
  
## <a name="digital-signature-features"></a><span data-ttu-id="b1f3a-106">Características de las firmas digitales</span><span class="sxs-lookup"><span data-stu-id="b1f3a-106">Digital Signature Features</span></span>

<span data-ttu-id="b1f3a-107">Las características de firmas digitales que proporciona InfoPath permiten:</span><span class="sxs-lookup"><span data-stu-id="b1f3a-107">The digital signatures features provided by InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="b1f3a-108">Habilitar las firmas para todo el formulario o para conjuntos específicos de datos del formulario que se puedan firmar por separado.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="b1f3a-p101">Especificar, por cada conjunto de datos que se pueda firmar, si se permiten una o varias firmas y la relación que tendrán. Por ejemplo, puede indicar si son cofirmas en paralelo o si cada nueva firma contrafirma todas las anteriores.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="b1f3a-111">Especificar un mensaje que se va a mostrar a los usuarios del formulario cuando lo firmen.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="b1f3a-112">Insertar y ver una firma en el documento.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="b1f3a-p102">Ver la información de no incumplimiento comprobable que se ha añadido a cada firma para incrementar la seguridad. Esta información adicional, que incluye una vista del formulario tal como se ha presentado a cada firmante, es una parte de la firma y no se puede quitar sin invalidar ésta. En cualquier momento, puede recuperar estos datos haciendo clic en la firma del formulario para mostrar el cuadro de diálogo **Comprobar firma digital**.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="b1f3a-p103">Sacar partido de un modelo de objetos para trabajar con firmas digitales. Añadir información personalizada al bloque de la firma de los formularios de plena confianza mediante el modelo de objetos de firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="b1f3a-118">Información general sobre el modelo de objetos de firmas digitales</span><span class="sxs-lookup"><span data-stu-id="b1f3a-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="the-sign-event"></a><span data-ttu-id="b1f3a-119">Evento Sign</span><span class="sxs-lookup"><span data-stu-id="b1f3a-119">The Sign Event</span></span>

<span data-ttu-id="b1f3a-120">El modelo de objetos de firmas digitales proporciona el siguiente evento.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="b1f3a-121">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-121">**Name**</span></span>|<span data-ttu-id="b1f3a-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f3a-123">Sign</span><span class="sxs-lookup"><span data-stu-id="b1f3a-123">Sign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |<span data-ttu-id="b1f3a-124">Se produce después de seleccionar un conjunto de datos para firmarlos.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-124">Occurs after a set of data has been selected to sign.</span></span>  <br/> <span data-ttu-id="b1f3a-p104">Puede utilizar este evento para manipular los datos almacenados en la firma digital. Por ejemplo, se pueden agregar datos de un servidor de marca de tiempo de confianza o agregar una contrafirma del lado servidor de la transacción. Asimismo, se puede usar este evento para bloquear la firma si el usuario actual no es integrante de un grupo determinado.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
### <a name="the-signeventargs-object"></a><span data-ttu-id="b1f3a-128">Objeto SignEventArgs</span><span class="sxs-lookup"><span data-stu-id="b1f3a-128">The SignEventArgs Object</span></span>

<span data-ttu-id="b1f3a-129">Un controlador de eventos para el evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) puede funcionar con el objeto del evento [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , que proporciona las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-129">An event handler for the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event can work with the [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) event object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="b1f3a-130">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-130">**Name**</span></span>|<span data-ttu-id="b1f3a-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f3a-132">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="b1f3a-132">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |<span data-ttu-id="b1f3a-133">Obtiene el conjunto de datos que ha producido el [evento Sign.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1f3a-133">Gets the set of data that raised the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event.</span></span>  <br/> |
|[<span data-ttu-id="b1f3a-134">SignatureWizard</span><span class="sxs-lookup"><span data-stu-id="b1f3a-134">SignatureWizard</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |<span data-ttu-id="b1f3a-135">Obtiene o establece información sobre si se debe mostrar el cuadro de diálogo **Firmas digitales**.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-135">Gets or sets whether to display the **Digital Signatures** dialog box.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b1f3a-p105">[!NOTA] En el modelo de objetos de código administrado de [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que acompañaba a InfoPath 2003, el objeto de evento [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) para el evento [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) proporciona una propiedad **XDocument** para tener acceso al objeto **XDocument** del formulario asociado con el evento. Esto no es necesario con las plantillas de formulario creadas con InfoPath Forms Services o InfoPath mediante el modelo de objetos de [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) porque puede tener acceso a los miembros del modelo de objetos de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) en el código de formulario usando la palabra clave **this** (C#) o **Me** (Visual Basic). Por ejemplo, para tener acceso a la propiedad [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para determinar si un formulario está firmado, puede escribir  `this.Signed` o  `Me.Signed.`</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p105">In the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) managed code object model that shipped with InfoPath 2003, the [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) event object for the [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) event provides an **XDocument** property for accessing the **XDocument** object of the form associated with the event. This is not necessary with form templates created with InfoPath Forms Services or InfoPath using the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) object model because the object model members of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class can be accessed in form code using the **this** (C#) or **Me** (Visual Basic) keyword. For example, to access the [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class to determine if a form is signed, you can type either  `this.Signed` or  `Me.Signed.`</span></span>
  
### <a name="collections-and-objects"></a><span data-ttu-id="b1f3a-139">Colecciones y objetos</span><span class="sxs-lookup"><span data-stu-id="b1f3a-139">Collections and Objects</span></span>

<span data-ttu-id="b1f3a-140">El modelo de objetos de firmas digitales proporciona las siguientes colecciones.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-140">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="b1f3a-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-141">**Name**</span></span>|<span data-ttu-id="b1f3a-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f3a-143">SignedDataBlockCollection</span><span class="sxs-lookup"><span data-stu-id="b1f3a-143">SignedDataBlockCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |<span data-ttu-id="b1f3a-144">La colección de los [objetos SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) de la plantilla de formulario tal como se define en tiempo de diseño en el modo de diseño de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-144">The collection of the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects in the form template as defined at design time in InfoPath design mode.</span></span>  <br/> <span data-ttu-id="b1f3a-145">La [colección SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementa propiedades que se pueden usar para tener acceso a los [objetos SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) asociados a un formulario.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-145">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) collection implements properties that can be used to access the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) objects associated with a form.</span></span> <span data-ttu-id="b1f3a-146">El [objeto SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) asociado a un formulario es accesible a través de la [propiedad SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) de la [clase XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1f3a-146">The [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) object associated with a form is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span>  <br/> |
|[<span data-ttu-id="b1f3a-147">SignatureCollection</span><span class="sxs-lookup"><span data-stu-id="b1f3a-147">SignatureCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |<span data-ttu-id="b1f3a-148">Contiene una colección de [objetos Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) para cada [objeto SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) del formulario.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-148">Contains a collection of [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects for each [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object in the form.</span></span>  <br/> <span data-ttu-id="b1f3a-149">La [clase SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implementa propiedades y un método que se pueden usar para tener acceso a los objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) asociados a un formulario y crear una firma.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-149">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class implements properties and a method that can be used to access a form's associated [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) objects and to create a signature.</span></span> <span data-ttu-id="b1f3a-150">El [objeto SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) asociado a [un SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) es accesible mediante la [propiedad Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1f3a-150">The [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) object associated with a [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) is accessible using the [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) property.</span></span>  <br/> <span data-ttu-id="b1f3a-151">Cuando use el [método CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la clase [SignatureCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) tenga en cuenta que la firma no se escribirá hasta que se llame al método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) en el [objeto Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1f3a-151">When you use the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method is called on the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object.</span></span> <span data-ttu-id="b1f3a-152">Solo se puede llamar a estos métodos desde el controlador de eventos **Sign** de una plantilla de formulario de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-152">These methods can be called only from the **Sign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="b1f3a-153">El modelo de objetos de firmas digitales proporciona los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-153">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="b1f3a-154">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-154">**Name**</span></span>|<span data-ttu-id="b1f3a-155">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1f3a-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1f3a-156">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="b1f3a-156">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="b1f3a-157">Representa un conjunto de datos que se pueden firmar en un formulario.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-157">Represents a set of signable data in a form.</span></span> <span data-ttu-id="b1f3a-158">El objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) proporciona una serie de propiedades y un método que se pueden usar para interactuar mediante programación con un conjunto de datos que se pueden firmar.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-158">The [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.</span></span>  <br/> |
|[<span data-ttu-id="b1f3a-159">Signature</span><span class="sxs-lookup"><span data-stu-id="b1f3a-159">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="b1f3a-160">Representa una firma digital agregada a un formulario o a un conjunto de datos que se pueden firmar de un formulario.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-160">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="b1f3a-161">El [objeto Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementa propiedades que se pueden usar para recuperar información sobre la firma digital y el método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) para escribir el bloque de firma digital XML e calcular su valor hash criptográfico.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-161">The [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="b1f3a-162">Certificado</span><span class="sxs-lookup"><span data-stu-id="b1f3a-162">Certificate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |<span data-ttu-id="b1f3a-163">Representa el certificado digital X.509 utilizado para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-163">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="b1f3a-164">Trabajar con firmas digitales mediante programación</span><span class="sxs-lookup"><span data-stu-id="b1f3a-164">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="b1f3a-p111">El modelo de objetos del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) ofrece miembros para interactuar con las firmas digitales mediante programación. Concretamente, los formularios de plena confianza pueden añadir información personalizada al bloque de la firma antes de confirmarlo, de acuerdo con la siguiente escala de tiempo:</span><span class="sxs-lookup"><span data-stu-id="b1f3a-p111">The object model of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span> 
  
1. <span data-ttu-id="b1f3a-167">El usuario elige añadir una firma digital a un formulario.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-167">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="b1f3a-168">Se muestra el cuadro de diálogo **Firmas digitales**, el usuario hace clic en **Agregar** y, después, selecciona los datos que se van a firmar.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-168">The **Digital Signatures** dialog box is displayed, the user clicks **Add**, and then selects the data to sign.</span></span>
    
3. <span data-ttu-id="b1f3a-169">Se inicia el evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) de los datos seleccionados que representa el objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) y se ejecutan el método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) del objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) y el método [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la colección [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1f3a-169">The [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event for the selected data represented by the [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object is raised, and the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method of [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) object and the [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) method of the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) collection are executed.</span></span> 
    
4. <span data-ttu-id="b1f3a-170">Se ejecutan todas las acciones personalizadas opcionales.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-170">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="b1f3a-171">Se ejecuta el método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) del objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b1f3a-171">The [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) method of the [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) object is executed.</span></span> 
    
6. <span data-ttu-id="b1f3a-172">El cuadro de diálogo **Firmar** se muestra para escribir un nombre (o seleccionar una imagen de firma), seleccionar un certificado con el que firmar y escribir comentarios.</span><span class="sxs-lookup"><span data-stu-id="b1f3a-172">The **Sign** dialog box is displayed for typing a name (or selecting a signature image), selecting a certificate to sign with, and to enter comments.</span></span> 
    
7. <span data-ttu-id="b1f3a-173">Cuando se hace clic en el botón **Firmar**, la firma se agrega a la colección de firmas del formulario y la información de no incumplimiento se capta y se guarda con la firma (que se puede ver más adelante haciendo clic en **Ver formulario firmado** en el cuadro de diálogo **Firmas digitales** y, después, haciendo clic en **Consultar la información de firma adicional que se recopiló**).</span><span class="sxs-lookup"><span data-stu-id="b1f3a-173">When the **Sign** button is clicked, the signature is added to the collection of signatures for the form and the non-repudiation information is captured and saved with the signature (which can be viewed later by clicking **View Signed Form** on the **Digital Signatures** dialog box, and then clicking **See the additional signing information that was collected**).</span></span>
    
<span data-ttu-id="b1f3a-174">En el ejemplo siguiente, se llama al método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) cuando un usuario firma los datos seleccionados y se contrafirma la firma con un valor de marca de tiempo recuperado de un servicio de marca de tiempo de confianza</span><span class="sxs-lookup"><span data-stu-id="b1f3a-174">The following example invokes the [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) method when the user signs the selected data and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


