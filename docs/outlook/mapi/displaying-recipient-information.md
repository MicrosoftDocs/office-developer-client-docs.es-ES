---
title: Mostrar información de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591292"
---
# <a name="displaying-recipient-information"></a>Mostrar información de destinatarios

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona un cuadro de diálogo común para que muestra los detalles de destinatario. El cuadro de diálogo detalles se crea a partir de una tabla para mostrar y una implementación de **IMAPIProp** . En la tabla para mostrar se describe la apariencia de la pantalla de detalles y la implementación de **IMAPIProp** controla los datos para el destinatario. Su proveedor es responsable de proporcionar la tabla para mostrar y la implementación de **IMAPIProp** para cada destinatario. 
  
La forma más sencilla de crear la tabla para mostrar es definir una estructura [DTPAGE](dtpage.md) y llamar a [BuildDisplayTable](builddisplaytable.md). Sin embargo, algunos proveedores, específicamente los proveedores de sólo lectura que permiten la creación de destinatarios de uso único, use **IPropData**. La implementación de **IMAPIProp** puede ser cualquier tipo de objeto de la propiedad. 
  
Existen dos métodos para llamar a este cuadro de diálogo: [IAddrBook::Details](iaddrbook-details.md) y [IMAPISupport::Details](imapisupport-details.md). Cuando el proveedor llama a uno de estos métodos para solicitar detalles de un destinatario, MAPI abre primero el destinatario mediante una llamada al método de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) de su contenedor. A continuación, se llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del destinatario para solicitar la propiedad de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** es la propiedad que representa la tabla de visualización de detalles de un destinatario. 
  
El [IPropData: IMAPIProp](ipropdataimapiprop.md) interfaz se puede usar para supervisar los cambios en los controles de tabla para mostrar tal como se describe en el procedimiento siguiente. 
  
## <a name="monitor-changes-to-a-control"></a>Supervisar los cambios en un control
  
1. Antes de que el usuario obtiene acceso al control, llame a [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para establecer el acceso de control en IPROP_CLEAN. 
    
2. Permitir que el usuario trabajar con el cuadro de diálogo. 
    
3. Cuando el usuario ha terminado, llame a [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar el nivel de acceso actual del control. 
    
4. Si el nivel de acceso es IPROP_DIRTY, el usuario ha modificado el control. Su proveedor debe:
    
   - Llame a [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) para establecer el acceso de nivel volver a IPROP_CLEAN. 
    
   - Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del objeto de datos de propiedad para recuperar la propiedad que ha cambiado y actualizar mediante una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Si el nivel de acceso sigue siendo IPROP_CLEAN, el control no se ha modificado. 
    
Para obtener más información sobre la creación de tablas para mostrar, vea [Mostrar tablas](display-tables.md).
  

