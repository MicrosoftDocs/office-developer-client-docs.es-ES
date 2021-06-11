---
title: Propiedad canónica PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436338"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propiedad canónica PidTagResourceMethods

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que indican los métodos de la interfaz **IMAPIStatus** que son compatibles con el objeto status. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificador:  <br/> |0x3E02  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad indica cuál de los métodos de la implementación de **IMAPIStatus** de un objeto de estado es compatible. Los objetos status pueden devolver MAPI_E_NO_SUPPORT de métodos no admitidos. 
  
Los clientes usan la propiedad PR_RESOURCE_METHODS de un objeto **de** estado para evitar realizar llamadas a métodos no compatibles. Si se establece la marca que corresponde a un método determinado, el método existe y se puede llamar. Si esa marca está clara, no se debe llamar al método. 
  
Los objetos de estado implementados por MAPI admiten los métodos siguientes:
  
|**Status (objeto)**|**Métodos admitidos**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState** only  <br/> |
|Libreta de direcciones MAPI  <br/> |**ValidateState** only  <br/> |
|Cola MAPI  <br/> |**ValidateState** y **FlushQueues** <br/> |
   
Una o varias de las siguientes marcas se pueden establecer en **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Indica que se admite [el método IMAPIStatus::ChangePassword.](imapistatus-changepassword.md) 
    
STATUS_FLUSH_QUEUES 
  
> Indica que se admite [el método IMAPIStatus::FlushQueues.](imapistatus-flushqueues.md) 
    
STATUS_SETTINGS_DIALOG 
  
> Indica que se admite [el método IMAPIStatus::SettingsDialog.](imapistatus-settingsdialog.md) 
    
STATUS_VALIDATE_STATE 
  
> Indica que se admite [el método IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

