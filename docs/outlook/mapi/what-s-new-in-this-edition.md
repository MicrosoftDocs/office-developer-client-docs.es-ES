---
title: Novedades de esta edición
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329550"
---
# <a name="whats-new-in-this-edition"></a>Novedades de esta edición

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La referencia MAPI de Microsoft Outlook 2013 se ha actualizado para incluir documentación para varias características nuevas. 
  
## <a name="new-content"></a>Nuevo contenido

Se ha agregado contenido para las siguientes características:
  
- El tema Introducción a la referencia MAPI de [Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) se ha actualizado para hacer referencia a información completa sobre modelos de programación para su funcionalidad de Outlook y MAPI para ayudarle a identificar las API y tecnologías más adecuadas para sus necesidades. Los vínculos al artículo técnico al que se hace referencia también se han revisado en los siguientes temas: 
    
  - [Referencia MAPI de Outlook](outlook-mapi-reference.md)
    
  - [Información general de la referencia de MAPI de Outlook](outlook-mapi-reference-overview.md)
    
- **Ejemplo del proveedor del almacén** de mensajes: el código del proveedor de almacén de [PST](message-store-provider-sample.md) ajustado de ejemplo se ha revisado para reconocer y dar cabida a Outlook 2013. Para obtener más información, vea Contenido revisado anteriormente en este tema. 
    
- **Secuencia de** autocompletar: el tema de caché de alias, anteriormente el formato de archivo **Nk2,** se ha actualizado para reflejar los cambios en Outlook 2013 y Outlook 2010. [](nickname-cache.md) Ahora se han revisado los siguientes temas para proporcionar información sobre las directrices para desarrolladores de formato de archivo .nk2 para Microsoft Outlook 2003/Microsoft Office Outlook 2007 y el análisis de archivos binarios. Para obtener más información, vea Contenido revisado anteriormente en este tema.
    
  - [Perfiles MAPI](mapi-profiles.md)
    
  - [Caché de alias](nickname-cache.md)
    
  - [Secuencia de autocompletar](autocomplete-stream.md)
    
- **Interfaces:** el tema [IAddrBook::OpenEntry](iaddrbook-openentry.md) documenta un método para abrir una entrada de la libreta de direcciones y devolver un puntero a la interfaz usada para obtener acceso a ella. Anteriormente contenía una marca en el parámetro  *ulFlags,* **MAPI_GAL_ONLY**, que se podía usar para abrir la lista global de direcciones (GAL), solo y se ha revisado para incluir su definición.
    
- **Propiedades:** el **PR_CONVERSATION_KEY** de la propiedad con nombre ( propiedad canónica [PidTagConversationKey](pidtagconversationkey-canonical-property.md)) se ha agregado y se relaciona con **IPM. Mensajes de MessageManager** solo en MAPI de Outlook. Se han revisado los siguientes temas relacionados con él y la Transport-Neutral de secuencias de formato de encapsulamiento de contenido (TNEF): 
    
  - [Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Asignación de atributos TNEF a propiedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID y attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Contenido revisado anteriormente

El contenido se agregó en versiones anteriores de la referencia MAPI de Outlook para las siguientes características:
  
- Microsoft Outlook 2013 permite escenarios de implementación no tradicionales, como hacer clic y ejecutar en paralelo. Estos escenarios pueden complicar la lógica usada para cargar la biblioteca MAPI adecuada. Los desarrolladores de MAPI ahora tienen la opción de vincular explícitamente a funciones MAPI y pueden elegir vincular explícitamente al código auxiliar MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Outlook) sin pasar por la biblioteca MAPI y el código auxiliar MAPI de Windows. Para obtener más información acerca de la vinculación explícita en comparación con la vinculación implícita, vea Vínculo a [funciones MAPI](how-to-link-to-mapi-functions.md). La biblioteca de códigos auxiliares **MAPI,** publicada en el sitio web [de CodePlex,](https://mapistublibrary.codeplex.com/) proporciona un reemplazo de lista desplegable para Mapi32.lib que admite la creación de aplicaciones MAPI de 32 bits y de 64 bits. 
    
- **Compatibilidad con Microsoft Outlook de 64** bits: los temas de referencia para los elementos de api aplicables se actualizaron para que se correspondan con los nuevos archivos de encabezado que admiten Outlook de 64 bits. Esos archivos de encabezado están disponibles como descarga [en Outlook 2010: Archivos de encabezado MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Se proporcionó un nuevo ejemplo de código en Comprobar la versión de [Outlook](how-to-check-the-version-of-outlook.md) para mostrar cómo comprobar si la versión instalada de Outlook es Microsoft Outlook 2010 de 64 bits y se ha revisado para Outlook 2013. Si la aplicación MAPI de 32 bits existente se va a ejecutar en un sistema operativo de 64 bits con Outlook de 64 bits instalado, tendrá que recompilar la aplicación de 32 bits como una aplicación de 64 bits. Para obtener más información acerca de la compatibilidad de MAPI con Outlook de 64 bits, vea Creación de aplicaciones MAPI en plataformas de [32 y 64 bits.](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)
    
- **Ejemplo del proveedor del almacén de** mensajes: el proveedor de almacenamiento [PST](message-store-provider-sample.md) ajustado de ejemplo se había actualizado anteriormente para admitir la arquitectura de 64 bits. El tema del ejemplo sobre la inicialización de un proveedor de almacén de [ARCHIVOS PST](initializing-a-wrapped-pst-store-provider.md) ajustados ahora se ha ampliado para proporcionar información sobre las "Rutas de acceso pst y Unicode ajustadas". 
    
- **Secuencia de** autocompletar: el tema de caché de alias, anteriormente el formato de archivo **Nk2,** se ha actualizado para reflejar los cambios en Outlook 2013 y Outlook 2010. [](nickname-cache.md) La información como la lista de autocompletar, que es la lista de nombres que se muestra en los cuadros [](autocomplete-stream.md) de edición Para **,** **CC** y **CCO** mientras un usuario está redactando un correo electrónico, ahora se guarda en la secuencia de Autocompletar de un mensaje en el equipo local en lugar de guardarlo en un archivo como en Outlook 2007. 
    
  - Interactuar con la secuencia de autocompletar
    
  - Cargar la secuencia de autocompletar
    
  - Guardar la secuencia de autocompletar
    
- **Compatibilidad con apagado rápido** para clientes MAPI: los clientes MAPI ahora pueden iniciar un apagado rápido y hacer que el subsistema MAPI notifique a los proveedores cargados para minimizar la pérdida de datos del apagado rápido. Se agregaron interfaces adicionales para que el cliente y el proveedor admitan el apagado rápido. Para obtener más información acerca del apagado rápido, vea [Cierre de cliente en MAPI.](client-shutdown-in-mapi.md)
    
- **Estructura de secuencias para definiciones de campo para** un elemento de Outlook: se agregó la documentación de una secuencia binaria para la propiedad [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) Esta propiedad especifica definiciones de todos los campos personalizados y la configuración de enlace de datos para los campos integrados de un elemento de Outlook. 
    
- **Invalidación de** almacén personal: se agregaron las siguientes interfaces y sus respectivos métodos para admitir la invalidación de la directiva **PSTDisableGrow** de proveedores de almacenamiento de carpetas personales (PST): 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Uso de varias cuentas de Exchange:** se agregó documentación para la API de libreta de direcciones [MAPI.](using-multiple-exchange-accounts.md) Esta API se mejoró para admitir varias cuentas de Exchange en Microsoft Outlook 2010 y ahora incluye Microsoft Outlook 2013. Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones. 
    
- **Formatos de archivo MAPI:** la información de configuración de MAPI se ha ampliado para explicar cómo se pueden usar rutas de acceso en Servicios de registro y proveedores de servicios [en MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propiedades:** se agregaron las siguientes propiedades etiquetadas además de la documentación de otras 38 propiedades etiquetadas y propiedades con nombre que se agregaron anteriormente:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI:** se han expandido las constantes [MAPI](mapi-constants.md) consolidadas. En versiones anteriores, se distribuían en varios temas, pero ahora se recopilan en un solo tema para que sean más fáciles de detectar y usar. También se han ampliado para proporcionar una cobertura más amplia, incluidas las siguientes secciones: 
    
  - Definiciones de códigos de error de la libreta de direcciones y del almacén de mensajes de Exchange
    
  - Definiciones para las cuotas Exchange Server modo caché de buzones de correo
    
## <a name="see-also"></a>Vea también



[Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

