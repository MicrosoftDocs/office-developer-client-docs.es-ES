---
title: Buscar un nombre de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407924"
---
# <a name="finding-a-profile-name"></a>Buscar un nombre de perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A veces, los clientes necesitan encontrar el nombre del perfil que se está utilizando actualmente para la sesión, el nombre del perfil predeterminado o el nombre de un perfil alternativo instalado en el equipo.
  
Hay varias formas de recuperar el nombre de un perfil durante el transcurso de una sesión. Si necesita encontrar el nombre de un perfil que no es necesariamente el que se usa para la sesión, use el primer procedimiento. Si necesita encontrar el nombre del perfil predeterminado, use el segundo procedimiento. Si necesita encontrar el nombre del perfil actual de la sesión, use el último procedimiento. 
  
 **Para buscar el nombre de cualquier perfil**
  
1. Llame [a MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin.** 
    
2. Llame [a IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles. 
    
3. Llame al método [IMAPITable::QueryRows](imapitable-queryrows.md) de la tabla de perfiles para recuperar todas las filas de la tabla y examinar cada una para determinar si representa el perfil de destino. 
    
 **Para buscar el nombre del perfil predeterminado**
  
1. Llame [a MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Llame [a IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles. 
    
3. Cree una restricción de propiedad con una [estructura SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) con el valor TRUE.
    
4. Llame [a IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila en la tabla de perfil que representa el perfil predeterminado. La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contiene el nombre del perfil predeterminado.
    
 **Para buscar el nombre del perfil actual**
  
Para buscar el nombre del perfil actual, siga uno de estos pasos:
  
- Suponiendo que tiene la estructura [MAPIUID](mapiuid.md) que representa una de las secciones del perfil actual, pásalo en el parámetro  _lpUID_ a [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Recupere la propiedad PR_PROFILE_NAME **de** la sección de perfil ([PidTagProfileName](pidtagprofilename-canonical-property.md)) mediante su [método IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
- Llame [a IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado y buscar la fila que tiene su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) establecida en MAPI_SUBSYSTEM. La **PR_DISPLAY_NAME** columna de esta fila es el nombre del perfil. No use la tabla de estado durante el inicio porque bloquea una aplicación hasta que la cola MAPI haya terminado de inicializar todos los proveedores de transporte. Esto puede degradar el rendimiento. 
    

