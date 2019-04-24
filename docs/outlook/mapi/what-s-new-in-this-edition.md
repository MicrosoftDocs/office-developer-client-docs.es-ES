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
  
La referencia MAPI de Microsoft Outlook 2013 se ha actualizado para incluir la documentación de varias características nuevas. 
  
## <a name="new-content"></a>Contenido nuevo

Se ha agregado contenido para las siguientes características:
  
- El tema [Introducción a la referencia MAPI de outlook 2013](getting-started-with-the-outlook-mapi-reference.md) se ha actualizado para hacer referencia a información completa sobre los modelos de programación para las funciones de Outlook y MAPI que le ayudarán a identificar las API y las tecnologías más adecuado para sus necesidades. Los vínculos al artículo técnico al que se hace referencia también se han revisado en los siguientes temas: 
    
  - [Referencia MAPI de Outlook](outlook-mapi-reference.md)
    
  - [Introducción a la referencia MAPI de Outlook](outlook-mapi-reference-overview.md)
    
- **Ejemplo de proveedor de almacén de mensajes**: ahora se ha revisado el código del [proveedor de almacén de archivos PST ajustado](message-store-provider-sample.md) para reconocer y acomodar Outlook 2013. Para obtener más información, vea contenido revisado previamente en este tema. 
    
- **Secuencia**de autocompletar: el tema de la [caché](nickname-cache.md) de sobrenombres, anteriormente el **formato de archivo Nk2**, se había actualizado para reflejar los cambios en Outlook 2013 y en Outlook 2010. Ahora se han revisado los temas siguientes para proporcionar información sobre el formato de archivo. NK2 para las directrices de desarrollador para Microsoft Outlook 2003/Microsoft Office Outlook 2007 y el análisis de archivos binarios. Para obtener más información, vea contenido revisado previamente en este tema.
    
  - [Perfiles MAPI](mapi-profiles.md)
    
  - [Caché de alias](nickname-cache.md)
    
  - [Secuencia de autocompletar](autocomplete-stream.md)
    
- **Interfaces**: el tema [IAddrBook:: OpenEntry](iaddrbook-openentry.md) documenta un método para abrir una entrada de la libreta de direcciones y devolver un puntero a la interfaz que se usa para tener acceso a ella. Anteriormente contenía una marca en el parámetro *ulFlags* , **MAPI_GAL_ONLY**, que podía usarse para abrir la lista global de direcciones (GAL), solo y se ha revisado para incluir su definición.
    
- **Propiedades**: se ha agregado el tema propiedad con nombre **PR_CONVERSATION_KEY** ([propiedad canónica PidTagConversationKey](pidtagconversationkey-canonical-property.md)) y está relacionado con **IPM. Mensajes MessageManager** en Outlook solo MAPI. Se han revisado los siguientes temas relacionados con ti y la documentación de la secuencia de formato de encapsulación neutro para el transporte (TNEF): 
    
  - [Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Asignación de atributos TNEF a propiedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID y attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Contenido revisado previamente

El contenido se agregó en versiones anteriores de la referencia MAPI de Outlook para las siguientes características:
  
- Microsoft Outlook 2013 permite escenarios de implementación no tradicionales, como en paralelo y hacer clic y ejecutar. Estos escenarios pueden complicar la lógica que se usa para cargar la biblioteca MAPI correcta. Ahora, los programadores de MAPI tienen la opción de vincular explícitamente a las funciones MAPI y pueden optar por establecer un vínculo explícito con el código auxiliar MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32. dll de Outlook) sin tener que pasar por la biblioteca MAPI y el código auxiliar MAPI de Windows. Para obtener más información sobre la vinculación explícita en comparación con la vinculación implícita, consulte [Link to MAPI Functions](how-to-link-to-mapi-functions.md). La **biblioteca de código auxiliar de MAPI**, publicada en el sitio web de [CodePlex](https://mapistublibrary.codeplex.com/) , proporciona un reemplazo de la lista para Mapi32. lib que admite la creación de aplicaciones MAPI de 32 bits y de 64 bits. 
    
- **Compatibilidad con Microsoft Outlook de 64**bits: los temas de referencia para los elementos de la API aplicables se actualizaron para coincidir con los nuevos archivos de encabezado que admiten Outlook de 64 bits. Estos archivos de encabezado están disponibles como descarga en [Outlook 2010: archivos de encabezado MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Se proporcionó un nuevo ejemplo de código en [comprobar la versión de Outlook](how-to-check-the-version-of-outlook.md) para mostrar cómo comprobar si la versión instalada de outlook es 64-bit de Microsoft Outlook 2010 y se ha revisado para Outlook 2013. Si la aplicación MAPI de 32 bits existente se va a ejecutar en un sistema operativo de 64 bits con Outlook de 64 bits instalado, tendrá que volver a crear la aplicación de 32 bits como una aplicación de 64 bits. Para obtener más información acerca de la compatibilidad de MAPI con Outlook de 64 bits, consulte [Building MAPI Applications on 32-bit and 64-bit Platforms](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Ejemplo de proveedor de almacenamiento de mensajes**: el [proveedor de almacén de archivos PST ajustado de muestra](message-store-provider-sample.md) se ha actualizado previamente para admitir la arquitectura de 64 bits. El ejemplo que [Inicializa un tema de proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md) ahora se ha ampliado para proporcionar información sobre el "archivo pst ajustado y las rutas de Unicode". 
    
- **Secuencia**de autocompletar: el tema de la [caché](nickname-cache.md) de sobrenombres, anteriormente el **formato de archivo Nk2**, se ha actualizado para reflejar los cambios en Outlook 2013 y en Outlook 2010. Información como la lista de autocompletar, que es la lista de nombres que se muestran en los cuadros de edición **para**, **CC**y **CCO** mientras un usuario redacta un correo electrónico, ahora se guarda en la secuencia de autocompletar de un mensaje en el equipo local [](autocomplete-stream.md) en lugar de guardarlo en un archivo como en Outlook 2007. 
    
  - Interacción con la secuencia de autocompletar
    
  - Cargar la secuencia de autocompletar
    
  - Guardar la secuencia de autocompletar
    
- **Compatibilidad con apagado rápido para clientes MAPI**: los clientes MAPI ahora pueden iniciar un apagado rápido y hacer que el subsistema MAPI notifique a los proveedores cargados para minimizar la pérdida de datos desde el apagado rápido. Se agregaron interfaces adicionales para el cliente y el proveedor para admitir el apagado rápido. Para obtener más información acerca del apagado rápido, consulte [Client Shutdown in MAPI](client-shutdown-in-mapi.md).
    
- **Estructura de secuencia para las definiciones de campo de un elemento de Outlook**: se ha agregado la documentación de una secuencia binaria para la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . Esta propiedad especifica las definiciones de todos los campos personalizados y la configuración de enlace de datos para los campos integrados de un elemento de Outlook. 
    
- **Reemplazo de almacén personal**: se han agregado las siguientes interfaces y sus métodos respectivos para admitir el reemplazo de la Directiva de **PSTDisableGrow** proveedores del almacén de archivos de carpetas personales (PST): 
    
    [IPSTOVERRIDEREQ:: IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1:: IUnknown](ipstoverride1iunknown.md)
    
- **Uso de varias cuentas de Exchange**: se ha agregado la documentación de la API de la [Libreta de direcciones MAPI](using-multiple-exchange-accounts.md) . Esta API se ha mejorado para admitir varias cuentas de Exchange en Microsoft Outlook 2010 y ahora incluye Microsoft Outlook 2013. Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones. 
    
- **Formatos de archivo MAPI**: la información de configuración MAPI se ha ampliado para explicar cómo se pueden usar las rutas de [registro de servicios y proveedores de servicios en MapiSvc. inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propiedades**: se agregaron las siguientes propiedades etiquetadas además de la documentación de 38 otras propiedades con etiquetas y propiedades con nombre que se han agregado anteriormente:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**: las constantes de [MAPI](mapi-constants.md) consolidadas se han expandido. En versiones anteriores, se distribuyeron en una serie de temas, pero ahora se recopilan en un solo tema para facilitar su detección y uso. También se han ampliado para proporcionar una cobertura más amplia, incluidas las secciones siguientes: 
    
  - Definiciones para los códigos de error de la libreta de direcciones de Exchange y el almacén de mensajes
    
  - Definiciones de cuotas del modo en caché del buzón de Exchange Server
    
## <a name="see-also"></a>Vea también



[Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

