---
title: Novedades de esta edición
manager: soliver
ms.date: 2/09/2020
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: 'Last modified: February 09, 2020'
ms.openlocfilehash: 3a3d38d83311b63686a2379c3321194e538ff840
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061331"
---
# <a name="whats-new-in-this-edition"></a>Novedades de esta edición

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La referencia mapi de Microsoft Outlook se ha actualizado para incluir documentación sobre varias características nuevas. 
  
## <a name="new-content"></a>Nuevo contenido

Se ha agregado contenido para las siguientes características:
  
- El tema Introducción a la referencia MAPI de [Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) se ha actualizado para hacer referencia a información completa acerca de los modelos de programación de la funcionalidad Outlook y MAPI para ayudarle a identificar las API y tecnologías más adecuadas para sus necesidades. También se han revisado los vínculos al artículo técnico al que se hace referencia en los temas siguientes: 
    
  - [Referencia MAPI de Outlook](outlook-mapi-reference.md)
    
  - [Información general de la referencia de MAPI de Outlook](outlook-mapi-reference-overview.md)
    
- **Ejemplo del proveedor del** almacén de mensajes: el código de proveedor de almacén [PST](message-store-provider-sample.md) ajustado de ejemplo ahora se ha revisado para reconocer y dar cabida a Outlook 2013. Para obtener más información, vea Contenido revisado anteriormente en este tema. 
    
- **Secuencia de** autocompletar: el tema de caché alias, anteriormente el formato de archivo **Nk2,** se había actualizado para reflejar los cambios en Outlook 2013 y en Outlook 2010. [](nickname-cache.md) Ahora se han revisado los temas siguientes para proporcionar información sobre las directrices para desarrolladores de formato de archivo .nk2 para Microsoft Outlook 2003/Microsoft Office Outlook 2007 y análisis de archivos binarios. Para obtener más información, vea Contenido revisado anteriormente en este tema.
    
  - [Perfiles MAPI](mapi-profiles.md)
    
  - [Caché de alias](nickname-cache.md)
    
  - [Secuencia de autocompletar](autocomplete-stream.md)
    
- **Interfaces**-The [IAddrBook::OpenEntry](iaddrbook-openentry.md) topic documents a method of opening an address book entry and returning a pointer to the interface used to access it. Anteriormente contenía una marca en el parámetro  *ulFlags,* **MAPI_GAL_ONLY**, que se podía usar para abrir la lista global de direcciones (GAL), solo y se ha revisado para incluir su definición.
    
- **Propiedades**: el **PR_CONVERSATION_KEY** con nombre ([PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md)) tema se ha agregado y está relacionado con **IPM. Mensajes messageManager** solo Outlook MAPI. Se han revisado los siguientes temas relacionados con él y la documentación Transport-Neutral de secuencia de formato de encapsulación (TNEF): 
    
  - [Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Asignación de atributos TNEF a propiedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID y attParentID](attconversationid-and-attparentid.md)
  
## <a name="mapi-initialization-monitor"></a>Monitor de inicialización MAPI  

- Hay ocasiones en las que una aplicación que consume MAPI puede querer saber cuándo se completa la inicialización. Por ejemplo, tiene varios subprocesos que podrían inicializar MAPI, o en respuesta a MAPI que se inicializa la aplicación le gustaría realizar algún trabajo, pero no quiere girar siempre la pila MAPI.  El monitor de inicialización proporciona esta funcionalidad a través de una función (exportada desde OLMAPI32.DLL) y un par de interfaces sencillas que se describen a continuación. 

### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor) 

- Este es el punto de entrada exportado desde OLMAPI32.DLL esto permite al autor de la llamada recuperar una interfaz para consultar el estado de inicialización actual, configurar una devolución de llamada para la finalización de inicialización o bloquear el subproceso actual hasta que se haya completado.  El objeto devuelto de esta API es reutilizable y seguro para subprocesos y se puede invocar desde cualquier subproceso, no solo desde el subproceso que la recuperó.  Además, a diferencia de otros objetos expuestos desde MAPI, este objeto es válido siempre que se cargue la DLL, se puede volver a usar en las sesiones de inicialización y se puede consumir antes o después de llamar a MAPIInitialize. Devuelve éxito o error a través de un HRESULT estándar COM y asigna un parámetro de salida a una instancia de IMAPIInitMonitor. 

### <a name="interface-imapiinitmonitor"></a>Interfaz: IMAPIInitMonitor 

**IFACEMETHODIMP_(BOOL) IsInitialized()**
- Devuelve el estado actual de inicialización MAPI 

**IFACEMETHODIMP Wait(DWORD timeout)**
- Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI.  INFINITE se puede usar para una espera infinita. 

**IFACEMETHODIMP BeginWait(DWORD timeout, IMAPIWaitResult ppResult)**
- Inicie una espera para que transcurra la inicialización MAPI o el número especificado de milisegundos.   Esto devuelve una interfaz IMAPIWaitResult que debería tener "End" llamado para comenzar la espera.  Esto permite al autor de la llamada controlar qué subproceso está bloqueado mientras estamos esperando. 

### <a name="interface-imapiwaitresult"></a>Interfaz IMAPIWaitResult
**Invalidación de IFACEMETHODIMP End()**
- Se llama para iniciar la espera de bloqueo en el subproceso al que se llama, no es necesario que sea el mismo subproceso que llamó a "BeginWait". 

    
## <a name="previously-revised-content"></a>Contenido revisado anteriormente

El contenido se agregó en versiones anteriores de Outlook referencia MAPI para las siguientes características:
  
- Microsoft Outlook 2013 permite escenarios de implementación no tradicionales, como en paralelo y Hacer clic y ejecutar. Estos escenarios pueden complicar la lógica usada para cargar la biblioteca MAPI adecuada. Los programadores MAPI ahora tienen la opción de vincular explícitamente a funciones MAPI y pueden elegir vincular explícitamente al código auxiliar MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Outlook) sin pasar por la biblioteca MAPI y el código auxiliar MAPI de Windows. Para obtener más información acerca de la vinculación explícita en comparación con la vinculación implícita, vea [Link to MAPI Functions](how-to-link-to-mapi-functions.md). La biblioteca de código auxiliar **MAPI**, publicada en el sitio web [codeplex,](https://mapistublibrary.codeplex.com/) proporciona un reemplazo de entrega para Mapi32.lib que admite la creación de aplicaciones MAPI de 32 bits y de 64 bits. 
    
- Compatibilidad con Microsoft Outlook de **64** bits: se actualizaron los temas de referencia para los elementos de API aplicables para que se correspondan con los nuevos archivos de encabezado que admiten archivos de 64 bits Outlook. Esos archivos de encabezado están disponibles como descarga [en Outlook 2010: Archivos de encabezado MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Se proporcionó un nuevo ejemplo de código en Comprobar la versión de [Outlook](how-to-check-the-version-of-outlook.md) para mostrar cómo comprobar si la versión instalada de Outlook es Microsoft Outlook 2010 de 64 bits y se ha revisado para Outlook 2013. Si la aplicación MAPI de 32 bits existente se va a ejecutar en un sistema operativo de 64 bits con Outlook de 64 bits instalado, deberá volver a compilar la aplicación de 32 bits como una aplicación de 64 bits. Para obtener más información acerca de la compatibilidad con MAPI para aplicaciones de 64 Outlook, vea [Building MAPI Applications on 32-Bit and 64-Bit Platforms](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Ejemplo del proveedor del** almacén de mensajes: el proveedor de almacén [PST](message-store-provider-sample.md) ajustado de ejemplo se había actualizado anteriormente para admitir la arquitectura de 64 bits. El tema Inicializar un proveedor de almacenamiento [PST](initializing-a-wrapped-pst-store-provider.md) ajustado del ejemplo ahora se ha expandido para proporcionar información sobre las "Rutas de acceso de Unicode y PST envueltas". 
    
- **Secuencia de** autocompletar: el tema de caché alias, anteriormente el formato de archivo **Nk2,** se ha actualizado para reflejar los cambios de Outlook 2013 y Outlook 2010. [](nickname-cache.md) Información como la lista de autocompletar, que es la lista  de nombres que se muestran en los cuadros de [](autocomplete-stream.md) edición Para **,** **Cc** y CCO mientras un usuario redacta un correo electrónico, ahora se guarda en la secuencia de autocompletar de un mensaje en el equipo local en lugar de guardarlo en un archivo como en Outlook 2007. 
    
  - Interactuar con la secuencia de autocompletar
    
  - Carga de la secuencia de autocompletar
    
  - Guardar la secuencia de autocompletar
    
- **Compatibilidad de apagado rápido** para clientes MAPI: los clientes MAPI ahora pueden iniciar un apagado rápido y hacer que el subsistema MAPI notifique a los proveedores cargados para minimizar la pérdida de datos del apagado rápido. Se agregaron interfaces adicionales para que el cliente y el proveedor admitan el apagado rápido. Para obtener más información sobre el apagado rápido, vea [Client Shutdown in MAPI](client-shutdown-in-mapi.md).
    
- **Estructura de secuencias para** definiciones de campo para un elemento Outlook :Se agregó documentación para una secuencia binaria para la [propiedad PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) Esta propiedad especifica definiciones de todos los campos personalizados y la configuración de enlace de datos para los campos integrados de un Outlook elemento. 
    
- **Invalidación de** almacén personal: se agregaron las interfaces siguientes y sus respectivos métodos para admitir la invalidación de la directiva de proveedores de almacenamiento **pstdisableGrow** de archivos de carpetas personales : 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Uso de varias Exchange :** se agregó la documentación de la API de libreta de direcciones [MAPI.](using-multiple-exchange-accounts.md) Esta API se ha mejorado para admitir varias Exchange cuentas en Microsoft Outlook 2010 y ahora incluye Microsoft Outlook 2013. Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones. 
    
- **Formatos de** archivo MAPI: se ha expandido la información de configuración de MAPI para explicar cómo se pueden usar rutas de acceso en Servicios de registro y proveedores de servicios [en MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propiedades**: las siguientes propiedades etiquetadas se agregaron además de la documentación de otras 38 propiedades etiquetadas y propiedades con nombre que se habían agregado anteriormente:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**: se han expandido las constantes [MAPI](mapi-constants.md) consolidadas. En versiones anteriores, se distribuían en varios temas, pero ahora se recopilan en un solo tema para que sean más fáciles de detectar y usar. También se han ampliado para proporcionar una cobertura más extensa, incluidas las siguientes secciones: 
    
  - Definiciones de códigos de error Exchange libreta de direcciones y almacén de mensajes
    
  - Definiciones de las Exchange Server de modo caché de buzón de correo
    
## <a name="see-also"></a>Vea también



[Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

