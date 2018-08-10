---
title: Firmar datos digitalmente en formularios de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Una firma digital es un sello electrónico seguro con cifrado de autenticación en una macro o documento. Una firma digital válida confirma que los datos provienen del firmante y no se han alterado desde que se firmaron. Cuando se firman documentos o ciertos datos de los documentos, se computa la firma y se agrega al documento. De esta manera, las firmas siempre viajarán con los datos firmados.
ms.openlocfilehash: dc839d0751d2e7aeb6f9eaccc3a86ce95e5228e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815848"
---
# <a name="digitally-signing-data-in-infopath-forms"></a><span data-ttu-id="4614b-106">Firmar datos digitalmente en formularios de InfoPath</span><span class="sxs-lookup"><span data-stu-id="4614b-106">Digitally Signing Data in InfoPath Forms</span></span>

<span data-ttu-id="4614b-p102">Una firma digital es un sello electrónico seguro con cifrado de autenticación en una macro o documento. Una firma digital válida confirma que los datos provienen del firmante y no se han alterado desde que se firmaron. Cuando se firman documentos o ciertos datos de los documentos, se computa la firma y se agrega al documento. De esta manera, las firmas siempre viajarán con los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="4614b-p102">A digital signature is an electronic, encryption-based, secure stamp of authentication on a macro or document. A valid digital signature confirms that the data originated from the signer and has not been altered since it was signed. When documents or certain data in the documents are signed, the signature is computed and added to the document. This way, the signatures will always travel with the signed data.</span></span>
  
<span data-ttu-id="4614b-p103">Para poder firmar datos, los usuarios tienen que solicitar un certificado a una entidad emisora de certificados y, a continuación, usarlo para crear firmas digitales. La entidad emisora de certificados administrará el ciclo de vida de los certificados y de las claves (públicas o privadas) necesarios para cifrar datos y crear la firma.</span><span class="sxs-lookup"><span data-stu-id="4614b-p103">In order to sign data, users need to request a certificate from a certificate authority, and then use it to create digital signatures. The certificate authority will manage the life cycle of the certificates and keys (public or private) needed to encrypt data and create the signature.</span></span>
  
<span data-ttu-id="4614b-p104">Los usuarios subsiguientes del documento deberán comprobar las firmas existentes y, de acuerdo con el resultado de la comprobación, podrán agregar su propia contribución y firmar. Para obtener resultados de comprobación exactos, el comprobador debe confiar en la entidad emisora de certificados que emitió el certificado que se usó para firmar el documento originalmente.</span><span class="sxs-lookup"><span data-stu-id="4614b-p104">Subsequent users of the document will have to verify existing signatures, and according to the result of the verification, may add their own contribution and sign. For accurate verification results, the verifier must trust the certificate authority who issued the certificate that was used to originally sign the document.</span></span>
  
<span data-ttu-id="4614b-p105">Las firmas digitales XML están diseñadas para transacciones que implican documentos y datos XML. El poder de las firmas XML se encuentra en la capacidad de firmar solamente datos específicos de un documento XML.</span><span class="sxs-lookup"><span data-stu-id="4614b-p105">XML digital signatures are designed for transactions that involve XML documents and data. The power of XML signatures stays in the ability to sign only specific data in an XML document.</span></span>
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a><span data-ttu-id="4614b-117">Tipos de firmas digitales en formularios de InfoPath</span><span class="sxs-lookup"><span data-stu-id="4614b-117">Types of Digital Signatures in InfoPath Forms</span></span>

<span data-ttu-id="4614b-p106">Microsoft InfoPath implementa firmas digitales para proteger los datos en formularios de InfoPath. En InfoPath, existen dos tipos de firmas digitales:</span><span class="sxs-lookup"><span data-stu-id="4614b-p106">Microsoft InfoPath implements digital signatures to help secure data in InfoPath forms. Two kinds of digital signatures are featured in InfoPath:</span></span>
  
- <span data-ttu-id="4614b-120">Firmas digitales que garantizan la integridad de los datos y la autenticidad de la plantilla de formulario (archivo .xsn)</span><span class="sxs-lookup"><span data-stu-id="4614b-120">Digital signatures that ensure the data integrity and authenticity of the form template (.xsn file)</span></span>
    
- <span data-ttu-id="4614b-121">Firmas digitales que garantizan la integridad, autenticidad y admisión de no rechazo en relación con datos de formularios XML</span><span class="sxs-lookup"><span data-stu-id="4614b-121">Digital signatures that ensure the integrity, authenticity, and support for non-repudiation related to data in XML forms</span></span>
    
<span data-ttu-id="4614b-p107">Mientras que la primera categoría de firmas está destinada a la plantilla de formulario (archivo .xsn), la segunda categoría está destinada a los datos reales ingresados por el usuario en los archivos de formulario de InfoPath (archivos .xml), donde el diseñador del formulario puede habilitar a los usuarios para crear firmas digitales para todo el formulario o para secciones del formulario. Hay diferencias fundamentales entre una plantilla firmada y un formulario firmado. Si bien este documento hará algunas referencias a las plantillas firmadas (como una forma alternativa de crear un formulario que se ejecutará como de plena confianza), no proporcionará detalles sobre este tipo de firma. Para obtener más información acerca de cómo firmar plantillas de formulario, vea el tema sobre [Implementar plantillas de formulario de InfoPath firmadas](deploying-signed-infopath-form-templates.md). Este tema se centra en el uso de formularios XML de InfoPath firmados. Las firmas digitales creadas por InfoPath para firmar datos en formularios XML cumplen con las especificaciones de las firmas digitales XML de W3C.</span><span class="sxs-lookup"><span data-stu-id="4614b-p107">Whereas the first category of signatures is targeting the form template (.xsn file), the second category targets the actual user-entered data in InfoPath form files (.xml files), where the form designer can enable users to create digital signatures for the whole form or for sections of the form. There are fundamental differences between a signed template and a signed form. Although this document will have some references to signed templates (as an alternative way to create a form that will run as fully trusted), it does not provide details about this kind of signing. For more information about how to sign form templates, see [Deploying Signed InfoPath Form Templates](deploying-signed-infopath-form-templates.md) The focus in this topic is using signed InfoPath XML forms. Digital signatures created by InfoPath to sign data in XML forms comply with W3C XML Digital Signatures specifications.</span></span> 
  
## <a name="digital-signatures-features"></a><span data-ttu-id="4614b-127">Características de las firmas digitales</span><span class="sxs-lookup"><span data-stu-id="4614b-127">Digital Signatures Features</span></span>

<span data-ttu-id="4614b-p108">InfoPath ofrece una amplia función de firmas digitales, que permite a los programadores de plantillas diseñar formularios flexibles que permitan firmas digitales tanto para todo el formulario como para datos específicos del formulario. Mientras que firmar todo el formulario siempre creará contrafirmas para el formulario como entidad, firmar partes de los formularios de InfoPath permite más flexibilidad al elegir el tipo de relación entre las firmas agregadas al mismo conjunto de datos: se pueden permitir cofirmas, contrafirmas o solamente una firma.</span><span class="sxs-lookup"><span data-stu-id="4614b-p108">InfoPath offers an extended digital signatures feature, with template developers being able to design flexible forms that enable digital signatures either for the whole form or for specific data in the form. Whereas digitally signing the whole form will always create counter-signatures for the form as an entity, signing parts of InfoPath forms enables more flexibility in choosing the kind of relationship between signatures added to the same set of data: there can be co-signatures, counter-signatures, or only one signature allowed.</span></span>
  
<span data-ttu-id="4614b-p109">Con la firma, InfoPath también agregará, de forma predeterminada, información de no rechazo para identificar a los usuarios de datos vistos en la vista actual, así como también la hora y otras configuraciones de entorno tal como estaban establecidas cuando se creó la firma. Se puede personalizar la información de no rechazo, pero solo se implementarán en el diálogo de no rechazo los datos de los nodos de no rechazo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4614b-p109">With the signature, InfoPath will also add by default some non-repudiation information to identify the data users have seen in the current view, as well as the time and other environment settings as they were set when the signature was created. The non-repudiation information can be customized, but only the data in default non-repudiation nodes will be displayed in the non-repudiation dialog.</span></span>
  
<span data-ttu-id="4614b-p110">Para agregar una firma, los usuarios tienen que seleccionar el conjunto de datos que se firmará. El conjunto de datos que se puede firmar lo define el diseñador de la plantilla de formulario y se usa para firmar los datos al rellenar el formulario. Para cada firma, los usuarios deberán seguir un asistente para firmas digitales para seleccionar el conjunto de datos que se pueden firmar, seleccionar un certificado, agregar comentarios, y aprobar y asignar la firma al formulario.</span><span class="sxs-lookup"><span data-stu-id="4614b-p110">In order to add a signature, users have to select the set of data that will be signed. The set of data that can be signed is defined by the form template designer and used to sign the data when filling out the form. For each signature, users will have to follow a digital signature wizard for selecting the set of signable data, selecting a certificate, adding comments, and approving and committing the signature to the form.</span></span>
  
<span data-ttu-id="4614b-p111">Cuando un usuario mantiene el mouse sobre un control que contiene datos firmados, InfoPath mostrará una indicación visual que advertirá de que los datos están firmados y no se pueden cambiar. Los diseñadores de plantillas de formulario pueden elegir que las firmas se muestren en la vista con los datos firmados para que los usuarios puedan tener un acceso fácil a la información de no rechazo.</span><span class="sxs-lookup"><span data-stu-id="4614b-p111">When a user rests the mouse over a control that contains signed data, InfoPath displays a visual indication that the data is signed and cannot be changed. Form template designers can choose to have the signatures displayed in the view with the signed data so that users can take advantage of easy access to the non-repudiation information.</span></span>
  
## <a name="programmatic-support-for-digital-signatures"></a><span data-ttu-id="4614b-137">Compatibilidad con firmas digitales mediante programación</span><span class="sxs-lookup"><span data-stu-id="4614b-137">Programmatic Support for Digital Signatures</span></span>

<span data-ttu-id="4614b-p112">El modelo de objetos de InfoPath incluye admisión de firmas digitales, lo que permite a los programadores un acceso mediante programación a los conjuntos de datos que se pueden firmar que se definen en el formulario mediante la clase [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , a las firmas asignadas a cada conjunto de datos firmados mediante la clase [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) y al certificado usado para crear una firma mediante la clase [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) . Además, el controlador de eventos [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) se personaliza en formularios de plena confianza, lo que ofrece compatibilidad con un procesamiento avanzado de firmas digitales en los formularios de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4614b-p112">The InfoPath object model includes support for digital signatures, which enables developers programmatic access to the sets of signable data are defined in the form through the [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) class, to the signatures assigned to each set of signed data through the [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) class, and to the certificate that is used to create a signature through the [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) class. Additionally, the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event handler is customizable in fully trusted forms, offering support for advanced processing of digital signatures in InfoPath forms.</span></span> 
  
## <a name="interoperability"></a><span data-ttu-id="4614b-140">Interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="4614b-140">Interoperability</span></span>

<span data-ttu-id="4614b-141">La infraestructura para firmas digitales de InfoPath se diseñó usando la compatibilidad con firmas digitales de MSXML5 para que las firmas digitales de InfoPath tengan interoperabilidad total con las firmas digitales de MSXML5.</span><span class="sxs-lookup"><span data-stu-id="4614b-141">The infrastructure for digital signatures in InfoPath was designed by using the digital signatures support in MSXML5 so that InfoPath digital signatures have full interoperability with MSXML5 digital signatures.</span></span>
  
<span data-ttu-id="4614b-p113">Los formularios de InfoPath firmados y las firmas digitales creadas por InfoPath también proporcionan interoperabilidad total con las firmas digitales creadas mediante Microsoft .NET Framework (a partir de la versión 1.1). Las firmas creadas por InfoPath se pueden comprobar con aplicaciones que usan clases de comprobación de firma de .NET Framework. Las firmas creadas para datos hospedados en formularios de InfoPath por aplicaciones diseñadas mediante clases de firmas digitales de .NET Framework se comprueban satisfactoriamente con el mecanismo de firmas digitales de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4614b-p113">Signed InfoPath forms and digital signatures created by InfoPath will also provide full interoperability with digital signatures created by using the Microsoft .NET Framework (starting with version 1.1). Signatures created by InfoPath can be verified by applications that use .NET Framework signature verification classes. Signatures created for data hosted in InfoPath forms by applications designed using .NET Framework digital signatures classes are successfully verified by InfoPath's digital signatures mechanism.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4614b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4614b-145">See also</span></span>



[<span data-ttu-id="4614b-146">Trabajar con firmas digitales</span><span class="sxs-lookup"><span data-stu-id="4614b-146">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
