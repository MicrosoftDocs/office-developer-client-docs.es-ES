---
title: Propiedad Hacer tipo de almacén privado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818068"
---
# <a name="make-store-type-private-property"></a>Propiedad Hacer tipo de almacén privado

  
  
**Hace referencia a**: Outlook 
  
Se trata de un almacén secundario como privada.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Tener acceso a ella:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta. Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #storetypeprivate"  <br/> |
   
Un proveedor de almacén puede utilizar esta propiedad para que Outlook lo tratan como privadas cuando se trata de un almacén secundario para un usuario. 
  
De forma predeterminada, Outlook trata un almacén secundario de la misma forma como un almacén delegado y los elementos en el almacén secundario son privados sólo si el usuario marca específicamente como privado. Cuando esta propiedad es **true**, los elementos eliminados de un almacén secundario se mueven a la carpeta **Elementos eliminados** en el almacén principal. No se muestran los elementos marcados como privados. Borradores se almacenan en la carpeta Borradores en el almacén principal. 
  
Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1, o si su valor es **false**.
  

