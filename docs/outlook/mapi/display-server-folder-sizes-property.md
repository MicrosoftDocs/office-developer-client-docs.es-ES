---
title: Propiedad Mostrar tamaño de carpetas de servidor
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
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816683"
---
# <a name="display-server-folder-sizes-property"></a>Propiedad Mostrar tamaño de carpetas de servidor

  
  
**Hace referencia a**: Outlook 
  
Muestra los tamaños de las carpetas especificadas en el servidor en el cuadro de diálogo **Tamaño de la carpeta** de Outlook. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Tener acceso a ella:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta. Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #serverfoldersizes"  <br/> |
   
Esta propiedad se admite en Microsoft Outlook 2003 Service Pack (SP) 1. Si la versión de Outlook es anterior a Outlook 2003 Service Pack 1, o si su valor es **false**, Outlook muestra sólo los tamaños de las carpetas en el almacén local. Si esta propiedad se establece en un almacén que usa Outlook 2003 SP 1, Outlook se consulta para el tamaño de cada carpeta especificada en el servidor y la unidad local. 
  
Para consultar el tamaño de la carpeta en el servidor, Outlook abre una carpeta en el almacén con [IMsgStore::OpenEntry](imsgstore-openentry.md), se pasa el indicador **MAPI_NO_CACHE**, y, a continuación, consulta para **PR_MESSAGE_SIZE_EXTENDED**. El proveedor de almacenamiento, a continuación, debe devolver el tamaño de la carpeta en el servidor.
  
Para consultar el tamaño de una carpeta en la unidad local, Outlook abre la carpeta sin el indicador **MAPI_NO_CACHE** . A continuación, se busca **PR_MESSAGE_SIZE_EXTENDED**; el proveedor de almacenamiento debe devolver el tamaño de la carpeta especificada en la unidad local.
  
Con este conjunto de propiedades, los proveedores de almacén que sincronización el almacén de contenido a un servidor pueden mostrar datos de tamaño de carpeta en el servidor en el cuadro de diálogo **Tamaño de la carpeta** de Outlook. Los usuarios, a continuación, pueden comparar su uso de almacenamiento de información de servidor actual con las cuotas de servidor. 
  

