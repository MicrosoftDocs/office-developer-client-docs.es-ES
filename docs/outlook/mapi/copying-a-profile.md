---
title: Copiar un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424731"
---
# <a name="copying-a-profile"></a>Copiar un perfil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una forma de crear un perfil es copiar desde un perfil existente y modificar los servicios de mensajes y los proveedores de servicios necesarios. La copia de un perfil implica el uso de un objeto de administración de perfil, proporcionado por MAPI a través de la [función MAPIAdminProfiles.](mapiadminprofiles.md) 
  
 **Para copiar un perfil**
  
1. Llame **a MAPIAdminProfiles** para recuperar un puntero de interfaz **IProfAdmin.** 
    
2. Llame [a IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles. 
    
3. Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del perfil que se va a copiar. 
    
4. Llame [a IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila adecuada en la tabla de perfiles. 
    
5. Llame [a IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)y pase el valor de **la columna PR_DISPLAY_NAME** como parámetro _lpszOldProfileName._ 
    

