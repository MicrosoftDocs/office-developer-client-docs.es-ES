---
title: Propiedad ocultar opción de actualización de reunión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299513"
---
# <a name="hide-meeting-update-option-property"></a>Propiedad ocultar opción de actualización de reunión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Oculta la opción de enviar actualizaciones de reunión solo a los asistentes agregados o eliminados.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto el:  <br/> |[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Se obtiene acceso mediante:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Lectura y escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionar cualquiera de las funciones de la tienda, el proveedor de almacenamiento debe implementar [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades que se pasan a una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp:: GetProps](imapiprop-getprops.md), el proveedor de almacén también debe devolver el valor de propiedad correcto. Los proveedores de almacenamiento pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe usar primero [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) a la que apunta el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # allornonemtgupdatedlg"  <br/> |
   
Un proveedor de almacenamiento que usa un servidor para enviar actualizaciones de reunión puede modificar el cuadro de diálogo **Enviar actualización a los asistentes** . Esta funcionalidad es útil porque cuando el servidor envía una actualización de la reunión, el servidor no sabe qué asistentes han sido agregados o eliminados por el usuario desde la solicitud de reunión inicial. Cuando esta propiedad es **true**, la opción **Enviar actualización sólo a los asistentes agregados o eliminados** no se muestra en el cuadro de diálogo **Enviar actualización a los asistentes** . 
  
Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1 o si su valor es **false**.
  

