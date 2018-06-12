---
title: Propiedad canónico PidTagResourceMethods
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820096"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propiedad canónico PidTagResourceMethods

  
  
**Se aplica a**: Outlook 
  
Contiene una máscara de bits de marcadores que indican los métodos en la interfaz de **IMAPIStatus** que son compatibles con el objeto de estado. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificador:  <br/> |0x3E02  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad indica cuál de los métodos de implementación de un objeto de estado de **IMAPIStatus** son compatibles. Se permiten los objetos de estado para devolver MAPI_E_NO_SUPPORT de métodos no admitidos. 
  
Los clientes utilizan la propiedad **PR_RESOURCE_METHODS** de un objeto estado para evitar la realización de llamadas a métodos no admitidos. Si se establece la marca que corresponde a un método concreto, el método existe y se puede llamar. Si esa marca está desactivada, no se debe llamar al método. 
  
Los objetos de estado implementan mediante la compatibilidad con MAPI los siguientes métodos:
  
|**Objeto de estado**|**Métodos admitidos**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState**  <br/> |
|Libreta de direcciones MAPI  <br/> |**ValidateState**  <br/> |
|Cola MAPI  <br/> |**ValidateState** y **FlushQueues** <br/> |
   
Uno o varios de los siguientes indicadores se pueden establecer en **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Indica que se admite el método [IMAPIStatus](imapistatus-changepassword.md) . 
    
STATUS_FLUSH_QUEUES 
  
> Indica que se admite el método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) . 
    
STATUS_SETTINGS_DIALOG 
  
> Indica que se admite el método [SettingsDialog](imapistatus-settingsdialog.md) . 
    
STATUS_VALIDATE_STATE 
  
> Indica que se admite el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

