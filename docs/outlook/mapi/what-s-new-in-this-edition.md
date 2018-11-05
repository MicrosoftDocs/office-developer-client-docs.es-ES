---
title: Novedades de esta edición
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Última modificación: 07 de diciembre de 2015'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392889"
---
# <a name="whats-new-in-this-edition"></a>Novedades de esta edición

 
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La referencia de MAPI de Microsoft Outlook 2013 se actualizó para incluir la documentación para varias características nuevas. 
  
## <a name="new-content"></a>Nuevo contenido

Se ha agregado el contenido de las siguientes características:
  
- El tema de [Introducción a la referencia de MAPI de Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) se ha actualizado para hacer referencia a información exhaustiva acerca de modelos de programación para la funcionalidad de Outlook y MAPI que le ayudarán a identificar las API y tecnologías que más adecuadas para sus necesidades. Vínculos a la que se hace referencia artículo técnico también se han revisado en los temas siguientes: 
    
  - [Referencia MAPI de Outlook](outlook-mapi-reference.md)
    
  - [Información general sobre la referencia MAPI de Outlook](outlook-mapi-reference-overview.md)
    
- **Ejemplo de proveedor de almacén de mensaje**: el código de [Ejemplo de proveedor de almacén de archivos PST ajustado](message-store-provider-sample.md) ahora se ha revisado para que reconozca y dar cabida a Outlook 2013. Para obtener más información, vea el contenido se revisó anteriormente en este tema. 
    
- **Secuencia de Autocompletar**: el tema de la [caché de sobrenombres](nickname-cache.md) , anteriormente el **Formato de archivo Nk2**, se había actualizado para reflejar los cambios en Outlook 2013, así como Outlook 2010. Ahora, los temas siguientes se han revisado para proporcionar información acerca de las directrices de desarrollador de formato de archivo. nk2 para Microsoft Outlook 2003 y Microsoft Office Outlook 2007 y análisis de archivos binarios. Para obtener más información, vea el contenido se revisó anteriormente en este tema.
    
  - [Perfiles de MAPI](mapi-profiles.md)
    
  - [Caché de alias](nickname-cache.md)
    
  - [Secuencia de Autocompletar](autocomplete-stream.md)
    
- **Interfaces**-el tema [IAddrBook::OpenEntry](iaddrbook-openentry.md) documenta un método para abrir una entrada de la libreta de direcciones y devolver un puntero a la interfaz que se usa para obtener acceso a él. Anteriormente, incluida una marca en el parámetro *ulFlags* , **MAPI_GAL_ONLY**, que puede usarse para abrir la Global lista direcciones (GAL), sólo y se ha revisado para incluir su definición.
    
- **Propiedades**: el **PR_CONVERSATION_KEY** con el nombre de tema de la propiedad ([Propiedad canónico PidTagConversationKey](pidtagconversationkey-canonical-property.md)) se ha agregado y se relaciona con **IPM. Objeto** sólo los mensajes de MAPI de Outlook. Se han revisado los siguientes temas relacionados con él y la documentación de secuencia de formato de encapsulación neutro para el transporte (TNEF): 
    
  - [Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Asignación de atributos TNEF a las propiedades de MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID y attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Contenido revisado anteriormente

Se ha agregado contenido en versiones anteriores de la referencia de MAPI de Outlook para las siguientes características:
  
- Microsoft Outlook 2013 permite escenarios de implementación no tradicionales como en paralelo y Click-to-Run. Estos escenarios pueden dificultar la lógica utilizada para cargar la biblioteca MAPI correcta. Los programadores MAPI ahora tienen la opción de vinculación explícitamente a las funciones MAPI y pueden elegir para vincularse explícitamente al código auxiliar MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Outlook) sin pasar por la biblioteca MAPI y el código auxiliar de MAPI de Windows. Para obtener más información acerca de la vinculación explícita en comparación con la vinculación implícita, vea el [vínculo a las funciones de MAPI](how-to-link-to-mapi-functions.md). La **Biblioteca de código auxiliar de MAPI**, registrado en el sitio Web de [CodePlex](https://mapistublibrary.codeplex.com/) , proporciona un reemplazo de orden para Mapi32.lib que admita la generación de aplicaciones de MAPI de 32 bits y 64 bits. 
    
- **Compatibilidad para Outlook de Microsoft de 64 bits**, temas de referencia para elementos de la API aplicables se actualizaron para corresponden a los nuevos archivos de encabezado que admiten Outlook de 64 bits. Los archivos de encabezado están disponibles como una descarga en [Outlook 2010: archivos de encabezado de MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Un ejemplo de código nuevo le ha proporcionado en [comprobar la versión de Outlook](how-to-check-the-version-of-outlook.md) para mostrar cómo comprobar si la versión de Outlook instalada es de 64 bits de Microsoft Outlook 2010 y se ha revisado para Outlook 2013. Si la aplicación existente de MAPI de 32 bits se va a ejecutar en un sistema operativo de 64 bits con Outlook de 64 bits instalado, debe volver a generar la aplicación de 32 bits como una aplicación de 64 bits. Para obtener más información sobre la compatibilidad de MAPI para Outlook de 64 bits, vea [Creación de aplicaciones MAPI en plataformas de 32 bits y 64 bits](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Ejemplo de proveedor de almacén de mensaje**: el [Proveedor de almacén de archivos PST ajustado de ejemplo](message-store-provider-sample.md) ya se ha actualizado para admitir la arquitectura de 64 bits. Tema de [inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md) del ejemplo ahora se ha ampliado para proporcionar información acerca de la "Wrapped PST y rutas de acceso Unicode." 
    
- **Secuencia de Autocompletar**: el tema de la [caché de sobrenombres](nickname-cache.md) , anteriormente el **Formato de archivo Nk2**, se ha actualizado para reflejar los cambios en Outlook 2013, así como Outlook 2010. Información como la lista de Autocompletar, que es la lista de nombres que se muestra en el **para**, **Cc**y **CCO** cuadros de edición mientras un usuario está redactando un correo electrónico, ahora se guarda en la [secuencia de Autocompletar](autocomplete-stream.md) de un mensaje en el equipo local en lugar de guardarlo en un archivo como se muestra en Outlook 2007. 
    
  - Interactuar con la secuencia de Autocompletar
    
  - Carga de la secuencia de Autocompletar
    
  - Guardar la secuencia de Autocompletar
    
- **Soporte técnico de apagado rápido para los clientes MAPI**, los clientes MAPI ahora pueden iniciar un cierre rápido y tienen el subsistema MAPI notificar a proveedores cargados para minimizar la pérdida de datos desde el apagado rápido. Se agregaron interfaces adicionales para que el cliente y el proveedor admite el apagado rápido. Para obtener más información acerca de apagado rápido, consulte [Apagado del cliente de MAPI](client-shutdown-in-mapi.md).
    
- **Estructura de la secuencia para las definiciones de campo para un elemento de Outlook**: se ha agregado la documentación para una secuencia binaria para la propiedad [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . Esta propiedad especifica las definiciones de todos los campos personalizados y configuración de enlace de datos para los campos integrados de un elemento de Outlook. 
    
- **Almacenar invalidar personales**: se han agregado las siguientes interfaces y sus respectivos métodos para admitir la invalidación de la directiva de **PSTDisableGrow** de proveedores de almacén de carpetas personales (PST) de archivo: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Uso de varias cuentas de Exchange**: se ha agregado la documentación para la [API de la libreta de direcciones de MAPI](using-multiple-exchange-accounts.md) . Esta API se ha mejorado para admitir varias cuentas de Exchange en Microsoft Outlook 2010 y ahora incluye Microsoft Outlook 2013. Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones. 
    
- **Los formatos de archivo de MAPI**: se ha ampliado la información de configuración de MAPI para explicar cómo puede usar rutas de acceso en el [registro de servicios y los proveedores de servicios MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propiedades**: se han agregado las siguientes propiedades con etiqueta además de documentación para 38 otros etiquetados propiedades y propiedades que tenían anteriormente se han agregado con nombre:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes de MAPI**: se han ampliado las consolidada [Constantes de MAPI](mapi-constants.md) . En versiones anteriores, que se han distribuido en un número de temas pero ahora se recopilan en un tema único para les que sea más fácil detectar y usar. También se han expandido para proporcionar una cobertura más amplia incluidos en las secciones siguientes: 
    
  - Definiciones de la libreta de direcciones de Exchange y los códigos de Error de almacén de mensajes
    
  - Cuotas de modo de caché de las definiciones para el buzón de correo de Exchange Server
    
## <a name="see-also"></a>Vea también



[Introducción a la referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

