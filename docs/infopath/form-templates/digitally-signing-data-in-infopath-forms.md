---
title: Firmar datos digitalmente en formularios de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Una firma digital es un sello electrónico seguro con cifrado de autenticación en una macro o documento. Una firma digital válida confirma que los datos provienen del firmante y no se han alterado desde que se firmaron. Cuando se firman documentos o ciertos datos de los documentos, se computa la firma y se agrega al documento. De esta manera, las firmas siempre viajarán con los datos firmados.
ms.openlocfilehash: 6c1f5a1c14c15bc88839dc44d9a5a595d8b52893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300248"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Firmar datos digitalmente en formularios de InfoPath

Una firma digital es un sello electrónico seguro con cifrado de autenticación en una macro o documento. Una firma digital válida confirma que los datos provienen del firmante y no se han alterado desde que se firmaron. Cuando se firman documentos o ciertos datos de los documentos, se computa la firma y se agrega al documento. De esta manera, las firmas siempre viajarán con los datos firmados.
  
Para poder firmar datos, los usuarios tienen que solicitar un certificado a una entidad emisora de certificados y, a continuación, usarlo para crear firmas digitales. La entidad emisora de certificados administrará el ciclo de vida de los certificados y de las claves (públicas o privadas) necesarios para cifrar datos y crear la firma.
  
Los usuarios subsiguientes del documento deberán comprobar las firmas existentes y, de acuerdo con el resultado de la comprobación, podrán agregar su propia contribución y firmar. Para obtener resultados de comprobación exactos, el comprobador debe confiar en la entidad emisora de certificados que emitió el certificado que se usó para firmar el documento originalmente.
  
Las firmas digitales XML están diseñadas para transacciones que implican documentos y datos XML. El poder de las firmas XML se encuentra en la capacidad de firmar solamente datos específicos de un documento XML.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Tipos de firmas digitales en formularios de InfoPath

Microsoft InfoPath implementa firmas digitales para proteger los datos en formularios de InfoPath. En InfoPath, existen dos tipos de firmas digitales:
  
- Firmas digitales que garantizan la integridad de los datos y la autenticidad de la plantilla de formulario (archivo .xsn)
    
- Firmas digitales que garantizan la integridad, autenticidad y admisión de no rechazo en relación con datos de formularios XML
    
Mientras que la primera categoría de firmas está destinada a la plantilla de formulario (archivo .xsn), la segunda categoría está destinada a los datos reales ingresados por el usuario en los archivos de formulario de InfoPath (archivos .xml), donde el diseñador del formulario puede habilitar a los usuarios para crear firmas digitales para todo el formulario o para secciones del formulario. Hay diferencias fundamentales entre una plantilla firmada y un formulario firmado. Si bien este documento hará algunas referencias a las plantillas firmadas (como una forma alternativa de crear un formulario que se ejecutará como de plena confianza), no proporcionará detalles sobre este tipo de firma. Para obtener más información acerca de cómo firmar plantillas de formulario, vea el tema sobre [Implementar plantillas de formulario de InfoPath firmadas](deploying-signed-infopath-form-templates.md). Este tema se centra en el uso de formularios XML de InfoPath firmados. Las firmas digitales creadas por InfoPath para firmar datos en formularios XML cumplen con las especificaciones de las firmas digitales XML de W3C. 
  
## <a name="digital-signatures-features"></a>Características de las firmas digitales

InfoPath ofrece una amplia función de firmas digitales, que permite a los programadores de plantillas diseñar formularios flexibles que permitan firmas digitales tanto para todo el formulario como para datos específicos del formulario. Mientras que firmar todo el formulario siempre creará contrafirmas para el formulario como entidad, firmar partes de los formularios de InfoPath permite más flexibilidad al elegir el tipo de relación entre las firmas agregadas al mismo conjunto de datos: se pueden permitir cofirmas, contrafirmas o solamente una firma.
  
Con la firma, InfoPath también agregará, de forma predeterminada, información de no rechazo para identificar a los usuarios de datos vistos en la vista actual, así como también la hora y otras configuraciones de entorno tal como estaban establecidas cuando se creó la firma. Se puede personalizar la información de no rechazo, pero solo se implementarán en el diálogo de no rechazo los datos de los nodos de no rechazo predeterminados.
  
Para agregar una firma, los usuarios tienen que seleccionar el conjunto de datos que se firmará. El conjunto de datos que se puede firmar lo define el diseñador de la plantilla de formulario y se usa para firmar los datos al rellenar el formulario. Para cada firma, los usuarios deberán seguir un asistente para firmas digitales para seleccionar el conjunto de datos que se pueden firmar, seleccionar un certificado, agregar comentarios, y aprobar y asignar la firma al formulario.
  
Cuando un usuario mantiene el mouse sobre un control que contiene datos firmados, InfoPath mostrará una indicación visual que advertirá de que los datos están firmados y no se pueden cambiar. Los diseñadores de plantillas de formulario pueden elegir que las firmas se muestren en la vista con los datos firmados para que los usuarios puedan tener un acceso fácil a la información de no rechazo.
  
## <a name="programmatic-support-for-digital-signatures"></a>Compatibilidad con firmas digitales mediante programación

El modelo de objetos de InfoPath incluye admisión de firmas digitales, lo que permite a los programadores un acceso mediante programación a los conjuntos de datos que se pueden firmar que se definen en el formulario mediante la clase [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , a las firmas asignadas a cada conjunto de datos firmados mediante la clase [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) y al certificado usado para crear una firma mediante la clase [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) . Además, el controlador de eventos [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) se personaliza en formularios de plena confianza, lo que ofrece compatibilidad con un procesamiento avanzado de firmas digitales en los formularios de InfoPath. 
  
## <a name="interoperability"></a>Interoperabilidad

La infraestructura para firmas digitales de InfoPath se diseñó usando la compatibilidad con firmas digitales de MSXML5 para que las firmas digitales de InfoPath tengan interoperabilidad total con las firmas digitales de MSXML5.
  
Los formularios de InfoPath firmados y las firmas digitales creadas por InfoPath también proporcionan interoperabilidad total con las firmas digitales creadas mediante Microsoft .NET Framework (a partir de la versión 1.1). Las firmas creadas por InfoPath se pueden comprobar con aplicaciones que usan clases de comprobación de firma de .NET Framework. Las firmas creadas para datos hospedados en formularios de InfoPath por aplicaciones diseñadas mediante clases de firmas digitales de .NET Framework se comprueban satisfactoriamente con el mecanismo de firmas digitales de InfoPath.
  
## <a name="see-also"></a>Vea también



[Trabajar con firmas digitales](how-to-work-with-digital-signatures.md)

