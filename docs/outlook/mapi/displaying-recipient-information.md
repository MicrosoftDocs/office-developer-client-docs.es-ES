---
title: Mostrar la información del destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412958"
---
# <a name="displaying-recipient-information"></a>Mostrar la información del destinatario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona un cuadro de diálogo común para mostrar los detalles del destinatario. El cuadro de diálogo de detalles se crea a partir de una tabla para mostrar y una **implementación de IMAPIProp.** La tabla para mostrar describe la apariencia de la presentación de detalles y la implementación **de IMAPIProp** controla los datos del destinatario. El proveedor es responsable de proporcionar la tabla para mostrar y la **implementación de IMAPIProp** para cada destinatario. 
  
La forma más sencilla de crear la tabla para mostrar es definir una [estructura DTPAGE](dtpage.md) y llamar a [BuildDisplayTable](builddisplaytable.md). Sin embargo, algunos proveedores, específicamente proveedores de solo lectura que permiten la creación de destinatarios únicos, usan **IPropData**. La **implementación de IMAPIProp** puede ser cualquier tipo de objeto de propiedad. 
  
Hay dos métodos para invocar este cuadro de diálogo: [IAddrBook::D etails](iaddrbook-details.md) e [IMAPISupport::D etails](imapisupport-details.md). Cuando el proveedor llama a uno de estos métodos para solicitar detalles para un destinatario, MAPI primero abre el destinatario llamando al método [IMAPIContainer::OpenEntry de](imapicontainer-openentry.md) su contenedor. A continuación, llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del destinatario para solicitar la **propiedad PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** es la propiedad que representa la tabla para mostrar detalles de un destinatario. 
  
La [interfaz IPropData : IMAPIProp](ipropdataimapiprop.md) se puede usar para supervisar los cambios en los controles de tabla para mostrar, tal como se describe en el siguiente procedimiento. 
  
## <a name="monitor-changes-to-a-control"></a>Supervisar cambios en un control
  
1. Antes de que el usuario obtenga acceso al control, llame a [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para establecer el acceso del control a IPROP_CLEAN. 
    
2. Permitir que el usuario trabaje con el cuadro de diálogo. 
    
3. Cuando el usuario haya terminado, llame a [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar el nivel de acceso actual del control. 
    
4. Si el nivel de acceso IPROP_DIRTY, el usuario ha modificado el control. El proveedor debe:
    
   - Llame [a IPropData::HrSetPropAccess para](ipropdata-hrsetpropaccess.md) volver a establecer el nivel de acceso en IPROP_CLEAN. 
    
   - Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del objeto de datos de propiedad para recuperar la propiedad modificada y actualizarla llamando a [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Si el nivel de acceso sigue IPROP_CLEAN, el control no se ha modificado. 
    
Para obtener más información acerca de la creación de tablas para mostrar, vea [Mostrar tablas](display-tables.md).
  

