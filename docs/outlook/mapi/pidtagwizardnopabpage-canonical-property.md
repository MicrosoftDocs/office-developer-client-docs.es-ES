---
title: Propiedad canónica PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424465"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Propiedad canónica PidTagWizardNoPabPage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene TRUE si el asistente para perfiles va a suprimir la página de libreta de direcciones personal (PAB).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Identificador:  <br/> |0x6701  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Administración de Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Los proveedores de servicios pueden establecer esta propiedad al llamar a una función basada en el prototipo de la función [LAUNCHWIZARDENTRY.](launchwizardentry.md) Esta propiedad indica al asistente para perfiles que el proveedor no desea que se muestre la página PAB durante el cuadro de diálogo de usuario. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

