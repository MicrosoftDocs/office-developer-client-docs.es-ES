---
title: Usar varias cuentas de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 3c0392cd6a885900c1a305cd1cd816a5925745a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398594"
---
# <a name="using-multiple-exchange-accounts"></a>Usar varias cuentas de Exchange

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten la integración con varias cuentas de correo electrónico de exchange. En Outlook 2010 o Outlook 2013, un usuario podr�a agregar dos cuentas de exchange para el mismo perfil y seguir disfrutando de las caracter�sticas avanzadas de Exchange, como la lista publicada global de direcciones (GAL), la configuraci�n de Exchange fuera de la oficina y uso compartido de carpetas.
  
Esos familiarizado con las secciones de perfil MAPI de Microsoft Office Outlook 2007 y versiones anteriores saben que la configuración de Exchange, como el nombre de usuario de correo electrónico y el nombre del servidor, se almacena en la sección de perfil de Exchange Global fija, **pbGlobalProfileSectionGuid**. Para obtener m�s informaci�n acerca del perfil Global de Exchange, vea [c�mo abrir la secci�n de perfil Global](https://support.microsoft.com/kb/188482). En Outlook 2010 y Outlook 2013, cada cuenta de Exchange necesita su propia secci�n de perfil para almacenar la configuraci�n, realizar la **pbGlobalProfileSectionGuid** obsoleto. 
  
Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Propiedad can�nico de PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.
  
Outlook 2010 y Outlook 2013 utilizan el **PidTagExchangeProfileSectionId** como un identificador �nico para especificar una cuenta de Exchange. Cuando se usa de esta manera, este identificador �nico se conoce como el **emsmdbUID**. Para algunas operaciones MAPI y Outlook, un **emsmdbUID** puede requerirse para especificar qu� cuenta de Exchange debe usarse para la operaci�n. 
  
In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Compatibilidad con heredado

Los clientes MAPI escritos antes de la creaci�n de esta nueva secci�n **emsmdbUID** a�n se admiten. Estos clientes seguir�n recuperar la secci�n global anterior, **pbGlobalProfileSectionGuid**. Las consultas de esta secci�n de perfil ser� redirigidas a una cuenta de Exchange designada que administra consultas heredadas. Puede determinar la cuenta que administra las llamadas heredadas busca en la tabla de servicios de mensaje y agregando una columna para PR_EMSMDB_LEGACY. Solo un servicio de mensaje tendr�n establecido en true y su **PidTagExchangeProfileSectionId** se denomina la heredado **emsmdbUID**.
  
> [!NOTE]
> [!NOTA] Opciones de configuraci�n de MAPI, como el almac�n predeterminado y la cuenta predeterminada de tengan ning�n efecto en el que cuenta controla las llamadas heredadas. No se puede configurar la cuenta que administra las llamadas heredadas. 
  
El **emsmdbUID** de la cuenta heredada se copian en la Outlook secci�n de perfil Global. Si esta propiedad no existe, la consulta de la tabla de servicios de mensaje determinar qu� cuenta es el controlador heredado y establecer el valor en la secci�n de perfil Global Outlook. 
  
Para borrar la Outlook que secci�n de perfil Global difiere de la secci�n de perfil Global de Exchange, y en Outlook 2010 y Outlook 2013 la secci�n de perfil Global de Exchange ya no es realmente global porque puede tener varias cuentas de Exchange. Outlook secci�n de perfil Global contiene propiedades de Outlook, como el estado de la carpeta de elementos utilizados Recientemente o el estado de la conexi�n global.
  
## <a name="address-book-account-contexts"></a>Contextos de cuenta de libreta de direcciones

Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones.
  
Algunos libreta de direcciones anterior API son obsoletas debido a las API no eran capaces de Exchange completamente varios. En este contexto de la cuenta normalmente es un **emsmdbUID**.
  
Adem�s de la **emsmdbUID**, varias cuentas de Exchange tienen un **emsabpUID**.
  
1. El valor de **emsmdbUID** identifica el contexto de la cuenta. 
    
2. El valor de **emsabpUID** identifica un proveedor de libreta de direcciones de Exchange. 
    
The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient. 
  
Si desea determinar el valor de **emsabpUID** para un determinado **emsmdbUID**, abra la secci�n de perfil para el **emsmdbUID** y obtener la propiedad **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.
  
Una descripci�n sencilla del proceso para la resoluci�n de varias cuentas de Exchange es el siguiente:
  
- Dado el identificador �nico del servicio, el c�digo busca en la tabla del almac�n de mensajes de la propiedad **PR_SERVICE_UID** que coincida con el que tiene. Desde all�, puede determinar la correcta **PR_MDB_PROVIDER**. Esta fila contiene el almac�n apropiado.
    
- Dado un **emsmdbUID**, el c�digo que se busca en la tabla de servicios de mensaje para la fila que expone el **PidTagExchangeProfileSectionId** que coincida con la **emsmdbUID**.
    
## <a name="see-also"></a>Vea tambi�n



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Propiedad can�nico de PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

