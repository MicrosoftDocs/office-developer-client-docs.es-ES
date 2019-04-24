---
title: Trabajar con firmas digitales mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007], infopath 2003-compatible form templates,InfoPath 2003-compatible form templates, digital signatures
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: El modelo de objetos compatible con InfoPath 2003 proporciona características para trabajar con firmas digitales mediante programación.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299912"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Trabajar con firmas digitales mediante el modelo de objetos de InfoPath 2003

El modelo de objetos compatible con InfoPath 2003 proporciona características para trabajar con firmas digitales mediante programación.
  
## <a name="digital-signature-features"></a>Características de las firmas digitales

Las características de firmas digitales disponibles en InfoPath permiten: 
  
- Habilitar las firmas para todo el formulario o para conjuntos específicos de datos del formulario que se puedan firmar por separado.
    
- Especificar, por cada conjunto de datos que se pueda firmar, si se permiten una o varias firmas y la relación que tendrán. Por ejemplo, puede indicar si son cofirmas en paralelo o si cada nueva firma contrafirma todas las anteriores.
    
- Especificar un mensaje que se va a mostrar a los usuarios del formulario cuando lo firmen.
    
- Insertar y ver una firma en el documento. 
    
- Ver la información de no incumplimiento comprobable que se ha añadido a cada firma para incrementar la seguridad. Esta información adicional, que incluye una vista del formulario tal como se ha presentado a cada firmante, es una parte de la firma y no se puede quitar sin invalidar ésta. En cualquier momento, puede recuperar estos datos haciendo clic en la firma del formulario para mostrar el cuadro de diálogo **Comprobar firma digital**. 
    
- Sacar partido de un modelo de objetos para trabajar con firmas digitales. Añadir información personalizada al bloque de la firma de los formularios de plena confianza mediante el modelo de objetos de firmas digitales. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Información general sobre el modelo de objetos de firmas digitales

### <a name="events"></a>Eventos

El modelo de objetos de firmas digitales proporciona el siguiente evento.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Se produce después de seleccionar un conjunto de datos para firmarlos.  <br/> Puede utilizar este evento para manipular los datos almacenados en la firma digital. Por ejemplo, se pueden agregar datos de un servidor de marca de tiempo de confianza o agregar una contrafirma del lado servidor de la transacción. Asimismo, se puede usar este evento para bloquear la firma si el usuario actual no es integrante de un grupo determinado.  <br/> |
   
El evento **OnSign** devuelve una referencia al objeto [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , que proporciona las siguientes propiedades. 
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Obtiene o establece un valor **Boolean** que indica el estado de retorno del evento **OnSign**.  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Obtiene el bloque de datos firmados que desencadenó el evento **OnSign**.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Obtiene una referencia al objeto **XDocument** asociado al evento **OnSign**.  <br/> |
   
### <a name="collections-and-objects"></a>Colecciones y objetos

El modelo de objetos de firmas digitales proporciona las siguientes colecciones.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |La colección de los objetos [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) de la plantilla de formulario tal como se define en el archivo de definición de formulario (. xsf).  <br/> La colección **SignedDataBlocksCollection** implementa propiedades que se pueden usar para obtener acceso a los objetos **SignedDataBlockObjects** asociados con un formulario. La colección **SignedDataBlocks** es accesible a través de la propiedad [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) del objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Contiene una colección de objetos [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) para cada **SignedDataBlockObject** del formulario.  <br/> La colección **SignaturesCollection** implementa propiedades y un método que se pueden usar para obtener acceso a objetos **SignatureObject** asociados con el formulario y crear una firma. Se puede obtener acceso a esta colección mediante el objeto **SignedDataBlockObject**.  <br/> Cuando se usa el método [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) de la colección **SignaturesCollection** , tenga en cuenta que la firma no se escribe hasta que se llama al método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) en el objeto **SignatureObject** Sólo se pueden llamar estos métodos desde el controlador de eventos **OnSign** de una plantilla de formulario de plena confianza.  <br/> |
   
El modelo de objetos de firmas digitales proporciona los siguientes objetos.
  
|**Nombre**|**Descripción**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Representa un conjunto de datos que se pueden firmar en un formulario. El objeto **SignedDataBlock** proporciona una serie de propiedades y un método que se pueden usar para interactuar mediante programación con un conjunto de datos que se pueden firmar.  <br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Representa una firma digital agregada a un formulario o a un conjunto de datos que se pueden firmar de un formulario. La colección **SignatureObject** implementa propiedades que se pueden usar para recuperar información sobre la firma digital y el método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) para escribir el bloque de firma digital XML y calcular el valor de hash criptográfico.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Representa el certificado digital X.509 utilizado para crear la firma.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabajar con firmas digitales mediante programación

El modelo de objetos compatible con InfoPath 2003 ofrece miembros para interactuar con las firmas digitales mediante programación. Concretamente, los formularios de plena confianza pueden añadir información personalizada al bloque de la firma antes de confirmarlo, de acuerdo con la siguiente escala de tiempo:
  
1. El usuario elige agregar una firma digital a un formulario.
    
2. Se muestra el primer panel del **Asistente para firmas digitales**. 
    
3. Se inicia el evento **OnSign** de los datos seleccionados que representa el objeto **SignedDataBlockObject** y se ejecutan el método **Sign** de **SignedDataBlockObject** y el método **Create** de **SignaturesCollection**. 
    
4. Se ejecutan todas las acciones personalizadas opcionales.
    
5. Se ejecuta el método **Sign** de **SignatureObject**. 
    
6. Se muestran el segundo y el tercer panel del asistente para seleccionar el certificado de la firma y escribir comentarios.
    
7. Se muestra la información de no incumplimiento (que se puede ver más tarde con el cuadro de diálogo **Comprobar firma digital**). 
    
8. Al hacer clic en el botón **Firmar**, se agrega la firma a la colección de firmas del formulario. 
    
En el ejemplo siguiente, se invoca el cuadro de diálogo **Firmar** y se contrafirma la firma con un valor de marca de tiempo recuperado de un servicio de marca de tiempo de confianza. 
  
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


