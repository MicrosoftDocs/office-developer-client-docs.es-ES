---
title: Propiedad Display Server Folder Sizes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434553"
---
# <a name="display-server-folder-sizes-property"></a>Propiedad Display Server Folder Sizes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra los tamaños de las carpetas especificadas en el servidor en el cuadro de diálogo Outlook **tamaño de** carpeta. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Creado por:  <br/> |Proveedor de la tienda  <br/> |
|Al que se accede mediante:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Lectura/escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionar cualquiera de las funciones del almacén, el proveedor de la tienda debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto. Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
Esta propiedad se admite en Microsoft Outlook 2003 Service Pack (SP) 1. Si la versión de Outlook es anterior a Outlook 2003 SP 1 o si su valor es **false,** Outlook mostrará solo los tamaños de carpetas en el almacén local. Si esta propiedad se establece en un almacén que usa Outlook 2003 SP 1, Outlook consultará el tamaño de cada carpeta especificada en el servidor y la unidad local. 
  
Para consultar el tamaño de carpeta en el servidor, Outlook abre una carpeta en el almacén con [IMsgStore::OpenEntry](imsgstore-openentry.md), pasando la marca **MAPI_NO_CACHE** y, a continuación, consulta **para PR_MESSAGE_SIZE_EXTENDED**. A continuación, el proveedor de almacenamiento debe devolver el tamaño de carpeta en el servidor.
  
Para consultar el tamaño de una carpeta en la unidad local, Outlook abre la carpeta sin la **marca MAPI_NO_CACHE.** A continuación, se consulta **PR_MESSAGE_SIZE_EXTENDED**; el proveedor de almacenamiento debe devolver el tamaño de la carpeta especificada en la unidad local.
  
Con este conjunto de propiedades, los proveedores de almacenamiento que sincronizan el contenido del almacén con un servidor pueden mostrar datos de tamaño de carpeta en el servidor en el cuadro de diálogo Outlook **tamaño** de carpeta. A continuación, los usuarios pueden comparar el uso actual del almacenamiento del servidor con las cuotas de servidor. 
  

