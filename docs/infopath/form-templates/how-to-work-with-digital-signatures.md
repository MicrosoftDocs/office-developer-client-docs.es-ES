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
# <a name="work-with-digital-signatures"></a>Trabajar con firmas digitales

El modelo de objetos del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) ofrece características para trabajar con firmas digitales mediante programación. 
  
## <a name="digital-signature-features"></a>Características de las firmas digitales

Las características de firmas digitales que proporciona InfoPath permiten: 
  
- Habilitar las firmas para todo el formulario o para conjuntos específicos de datos del formulario que se puedan firmar por separado.
    
- Especificar, por cada conjunto de datos que se pueda firmar, si se permiten una o varias firmas y la relación que tendrán. Por ejemplo, puede indicar si son cofirmas en paralelo o si cada nueva firma contrafirma todas las anteriores.
    
- Especificar un mensaje que se va a mostrar a los usuarios del formulario cuando lo firmen.
    
- Insertar y ver una firma en el documento. 
    
- Ver la información de no incumplimiento comprobable que se ha añadido a cada firma para incrementar la seguridad. Esta información adicional, que incluye una vista del formulario tal como se ha presentado a cada firmante, es una parte de la firma y no se puede quitar sin invalidar ésta. En cualquier momento, puede recuperar estos datos haciendo clic en la firma del formulario para mostrar el cuadro de diálogo **Comprobar firma digital**. 
    
- Sacar partido de un modelo de objetos para trabajar con firmas digitales. Añadir información personalizada al bloque de la firma de los formularios de plena confianza mediante el modelo de objetos de firmas digitales. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Información general sobre el modelo de objetos de firmas digitales

### <a name="the-sign-event"></a>Evento Sign

El modelo de objetos de firmas digitales proporciona el siguiente evento.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Se produce después de seleccionar un conjunto de datos para firmarlos.  <br/> Puede utilizar este evento para manipular los datos almacenados en la firma digital. Por ejemplo, se pueden agregar datos de un servidor de marca de tiempo de confianza o agregar una contrafirma del lado servidor de la transacción. Asimismo, se puede usar este evento para bloquear la firma si el usuario actual no es integrante de un grupo determinado.  <br/> |
   
### <a name="the-signeventargs-object"></a>Objeto SignEventArgs

Un controlador de eventos para el evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) puede funcionar con el objeto del evento [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) , que proporciona las siguientes propiedades. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Obtiene el conjunto de datos que provocó el evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) .  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Obtiene o establece información sobre si se debe mostrar el cuadro de diálogo **Firmas digitales**.  <br/> |
   
> [!NOTE]
> [!NOTA] En el modelo de objetos de código administrado de [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) que acompañaba a InfoPath 2003, el objeto de evento [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) para el evento [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) proporciona una propiedad **XDocument** para tener acceso al objeto **XDocument** del formulario asociado con el evento. Esto no es necesario con las plantillas de formulario creadas con InfoPath Forms Services o InfoPath mediante el modelo de objetos de [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) porque puede tener acceso a los miembros del modelo de objetos de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) en el código de formulario usando la palabra clave **this** (C#) o **Me** (Visual Basic). Por ejemplo, para tener acceso a la propiedad [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) para determinar si un formulario está firmado, puede escribir  `this.Signed` o  `Me.Signed.`
  
### <a name="collections-and-objects"></a>Colecciones y objetos

El modelo de objetos de firmas digitales proporciona las siguientes colecciones.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |La colección de los objetos [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) de la plantilla de formulario como se define en tiempo de diseño en el modo de diseño de InfoPath.  <br/> La colección [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementa propiedades que se pueden usar para tener acceso a los objetos [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) asociados a un formulario. Se puede tener acceso al objeto [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) asociado a un formulario a través de la propiedad [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Contiene una colección de objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) para cada objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) del formulario.  <br/> La clase [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implementa propiedades y un método que se pueden usar para tener acceso a los objetos [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) asociados de un formulario y para crear una firma. El objeto [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) asociado a un objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) es accesible mediante la propiedad [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) .  <br/> Cuando use el método [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la clase [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , tenga en cuenta que la firma no se escribe hasta que se llama al método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) en el objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . Solo se puede llamar a estos métodos desde el controlador de eventos **Sign** de una plantilla de formulario de plena confianza.  <br/> |
   
El modelo de objetos de firmas digitales proporciona los siguientes objetos.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Representa un conjunto de datos que se pueden firmar en un formulario. El objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) proporciona una serie de propiedades y un método que se pueden usar para interactuar mediante programación con un conjunto de datos que se pueden firmar.  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Representa una firma digital agregada a un formulario o a un conjunto de datos que se pueden firmar de un formulario. El objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementa propiedades que se pueden usar para recuperar información sobre la firma digital y el método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) para escribir el bloque de firma digital XML y calcular el valor de hash criptográfico.  <br/> |
|[Certificado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Representa el certificado digital X.509 utilizado para crear la firma.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabajar con firmas digitales mediante programación

El modelo de objetos del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) ofrece miembros para interactuar con las firmas digitales mediante programación. Concretamente, los formularios de plena confianza pueden añadir información personalizada al bloque de la firma antes de confirmarlo, de acuerdo con la siguiente escala de tiempo: 
  
1. El usuario elige añadir una firma digital a un formulario.
    
2. Se muestra el cuadro de diálogo **Firmas digitales**, el usuario hace clic en **Agregar** y, después, selecciona los datos que se van a firmar.
    
3. Se inicia el evento [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) de los datos seleccionados que representa el objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) y se ejecutan el método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) del objeto [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) y el método [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la colección [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) . 
    
4. Se ejecutan todas las acciones personalizadas opcionales.
    
5. Se ejecuta el método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) del objeto [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . 
    
6. El cuadro de diálogo **Firmar** se muestra para escribir un nombre (o seleccionar una imagen de firma), seleccionar un certificado con el que firmar y escribir comentarios. 
    
7. Cuando se hace clic en el botón **Firmar**, la firma se agrega a la colección de firmas del formulario y la información de no incumplimiento se capta y se guarda con la firma (que se puede ver más adelante haciendo clic en **Ver formulario firmado** en el cuadro de diálogo **Firmas digitales** y, después, haciendo clic en **Consultar la información de firma adicional que se recopiló**).
    
En el ejemplo siguiente, se llama al método [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) cuando un usuario firma los datos seleccionados y se contrafirma la firma con un valor de marca de tiempo recuperado de un servicio de marca de tiempo de confianza 
  
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


