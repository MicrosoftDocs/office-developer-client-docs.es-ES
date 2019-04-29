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
  
MAPI proporciona un cuadro de diálogo común para mostrar los detalles de los destinatarios. El cuadro de diálogo Detalles se crea a partir de una tabla de presentación y una implementación de **IMAPIProp** . La tabla de visualización describe la apariencia de la visualización de detalles y la implementación de **IMAPIProp** controla los datos para el destinatario. El proveedor es responsable de suministrar la tabla de presentación y la implementación de **IMAPIProp** para cada destinatario. 
  
La forma más sencilla de crear la tabla de visualización es definir una estructura [DTPAGE](dtpage.md) y llamar a [BuildDisplayTable](builddisplaytable.md). Sin embargo, algunos proveedores, específicamente los proveedores de solo lectura que permiten la creación de destinatarios únicos, usan **IPropData**. La implementación de **IMAPIProp** puede ser cualquier tipo de objeto Property. 
  
Hay dos métodos para invocar este cuadro de diálogo: [IAddrBook::D etails](iaddrbook-details.md) y [IMAPISupport::D etails](imapisupport-details.md). Cuando el proveedor llama a uno de estos métodos para solicitar detalles para un destinatario, MAPI abre primero el destinatario mediante una llamada al método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) del contenedor. A continuación, llama al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del destinatario para solicitar la propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** es la propiedad que representa la tabla de visualización de detalles de un destinatario. 
  
La interfaz [IPropData: IMAPIProp](ipropdataimapiprop.md) se puede usar para supervisar los cambios en los controles de la tabla de visualización tal como se describe en el siguiente procedimiento. 
  
## <a name="monitor-changes-to-a-control"></a>Supervisión de los cambios en un control
  
1. Antes de que el usuario obtenga acceso al control, llame a [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) para establecer el acceso del control a IPROP_CLEAN. 
    
2. Permite al usuario trabajar con el cuadro de diálogo. 
    
3. Cuando el usuario haya finalizado, llame a [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar el nivel de acceso actual del control. 
    
4. Si el nivel de acceso es IPROP_DIRTY, el usuario ha modificado el control. El proveedor debe:
    
   - Llame a [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) para volver a establecer el nivel de acceso en IPROP_CLEAN. 
    
   - Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto de datos de propiedad para recuperar la propiedad modificada y actualizarla llamando a [IMAPIProp:: SetProps](imapiprop-setprops.md).
    
5. Si el nivel de acceso sigue siendo IPROP_CLEAN, no se ha modificado el control. 
    
Para obtener más información acerca de la creación de tablas de visualización, consulte [Display tables](display-tables.md).
  

