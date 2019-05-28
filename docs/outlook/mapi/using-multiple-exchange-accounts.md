---
title: Usar varias cuentas de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329658"
---
# <a name="using-multiple-exchange-accounts"></a>Usar varias cuentas de Exchange

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten la integración con varias cuentas de correo electrónico de Exchange. En Outlook 2010 o Outlook 2013, un usuario podía añadir dos cuentas de Exchange al mismo perfil y seguir disfrutando de las características enriquecidas de Exchange, como la lista global de direcciones (GAL), la configuración Fuera de la Oficina de Exchange y el uso compartido de carpetas.
  
Quienes ya conocían las secciones de perfil MAPI de Microsoft Office Outlook 2007 y versiones anteriores sabían que la configuración de Exchange, como el nombre de usuario de correo electrónico y el nombre de servidor, se almacenaba en la sección fijada de Perfil Global de Exchange, **pbGlobalProfileSectionGuid**. En Outlook 2010 y Outlook 2013, todas las cuentas de Exchange necesitan su propia sección de perfil para almacenar la configuración, lo que vuelve obsoleto **pbGlobalProfileSectionGuid**. 
  
Las opciones de configuración de Exchange 2010 y Outlook 2013 siguen almacenadas en el perfil, pero se asigna dinámicamente para cada perfil un identificador único para la sección de perfil que contiene su configuración. La ubicación de la configuración de Exchange en el perfil se almacena en la [Propiedad Canónica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que se puede encontrar en la sección de perfil de servicio de mensajes de la cuenta de Exchange. Esta propiedad también se puede encontrar en la sección de perfil para cada proveedor en este servicio de mensaje de la cuenta. El identificador único no se almacena en el servidor y varía en los distintos perfiles.
  
Outlook 2010 y Outlook 2013 usan **PidTagExchangeProfileSectionId** como identificador único para especificar una cuenta de Exchange. Cuando se usa de esta manera, este identificador único se denomina **emsmdbUID**. En algunas operaciones MAPI y Outlook, es posible que se necesite un **emsmdbUID** para especificar la cuenta de Exchange que se debe usar para la operación. 
  
A fin de admitir varias cuentas de Exchange, se deben usar algunas llamadas a las nuevas funciones en su código. Reemplace cualquier llamada que utilice una **entryID** y una [IAddrBook::OpenEntry](iaddrbook-openentry.md) o [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) en [IMailUser : IMAPIProp](imailuserimapiprop.md), así como [IDistList : IMAPIContainer](idistlistimapicontainer.md), por una de las funciones siguientes. 
  
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
    
## <a name="legacy-support"></a>Soporte técnico heredado

Se siguen admitiendo todos los clientes MAPI escritos antes de la creación de esta nueva sección **emsmdbUID**. Estos clientes seguirán recuperando la sección global anterior, **pbGlobalProfileSectionGuid**. Las consultas de esta sección de perfil se redirigirán a una cuenta de Exchange designada que controla las consultas heredadas. La cuenta que controla las llamadas heredadas se puede determinar buscando en la tabla de servicio de mensajes y agregando una columna para PR_EMSMDB_LEGACY. Solo un único servicio de mensajes la tendrá definida como true y su **PidTagExchangeProfileSectionId** se denomina **emsmdbUID** heredado.
  
> [!NOTE]
> Las opciones de ajustes de MAPI configurables, como el almacenamiento predeterminada y la cuenta predeterminada, no tienen ningún efecto en la cuenta que realiza llamadas heredadas. No se puede configurar la cuenta que controla las llamadas heredadas. 
  
El **emsmdbUID** de la cuenta heredada se copia a la sección del perfil global de Outlook. Si esta propiedad no existe, una consulta a la tabla de servicios de mensajes determinará qué cuenta es el controlador heredado y establecerá el valor en la sección de perfil global de Outlook. 
  
Para mayor claridad, la sección de perfil global de Outlook es diferente de la sección de perfil global de Exchange y, en Outlook 2010 y Outlook 2013, la sección de perfil global de Exchange ya no es realmente global, puesto que se pueden tener varias cuentas de Exchange. La sección perfil global de Outlook contiene propiedades sobre Outlook, como el estado de la carpeta MRU o el estado de la conexión global.
  
## <a name="address-book-account-contexts"></a>Contextos de cuenta de la libreta de direcciones

Para resolver las direcciones correctamente con varias cuentas de Exchange, use las nuevas funciones que toman un contexto de cuenta para que las llamadas a la libreta de direcciones busquen la cuenta de Exchange adecuada.
  
Algunas API de libreta de direcciones anteriores eran obsoletas porque las API no eran totalmente compatibles con Exchange. Este contexto de cuenta suele ser un **emsmdbUID**.
  
Además del **emsmdbUID**, las cuentas múltiples de Exchange también tienen un **emsabpUID**.
  
1. El valor de **emsmdbUID** identifica el contexto de la cuenta. 
    
2. El valor de **emsabpUID** identifica un proveedor de libreta de direcciones de Exchange. 
    
El valor de **emsabpUID** se utiliza habitualmente al resolver un destinatario. Al resolver un destinatario utilizando [IAddrBook::ResolveName](iaddrbook-resolvename.md), una fila de destinatario de Exchange puede contener la propiedad **PR_AB_PROVIDERS** (0x3D010102), que contiene el valor de **emsabpUID**. Este valor de **emsabpUID** identifica el proveedor de libreta de direcciones de Exchange para el destinatario específico. 
  
Si desea determinar el valor de **emsabpUID** para un **emsmdbUID** concreto, abra la sección de perfil del **emsmdbUID** y obtenga la propiedad **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
Si está llamando a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), asegúrese de que los destinatarios de Exchange de la lista que pase contengan la propiedad **PR_AB_PROVIDERS** que tiene el **emsabpUID** que corresponde al proveedor de libreta de direcciones al que pertenece el destinatario. Para llamar a un [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) en una fila que ha obtenido desde [IAddrBook::ResolveName](iaddrbook-resolvename.md) no requiere realizar acciones adicionales, pero el código llamará a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) en filas que únicamente contienen la propiedad **PR_ENTRYID**. Las filas en esta situación y en situaciones similares deberían contener **PR_ENTRYID** y **PR_AB_PROVIDERS** con la propiedad **PR_AB_PROVIDERS** ajustada para el **emsabpUID** correcto.
  
Una descripción simple del proceso para resolver varias cuentas de Exchange es la siguiente:
  
- Dado el identificador único de servicio, el código busca en la tabla el almacén de mensajes de la propiedad **PR_SERVICE_UID** que coincide con la única que se dispone. A partir de ahí, se puede determinar el **PR_MDB_PROVIDER** correcto. Esta fila contiene el almacén adecuado.
    
- Dado un **emsmdbUID**, su código busca en la tabla de servicios de mensaje la fila que expone el **PidTagExchangeProfileSectionId** que coincide con el **emsmdbUID**.
    
## <a name="see-also"></a>Vea también



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
  
[Propiedad Canónica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[Cómo abrir la sección Perfil global](https://support.microsoft.com/kb/188482)

