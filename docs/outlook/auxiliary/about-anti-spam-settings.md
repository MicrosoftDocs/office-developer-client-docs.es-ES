---
title: Información sobre la configuración contra correo no deseado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permite a los usuarios especificar la configuración para cada cuenta para ayudar a proteger la cuenta contra correo no deseado. Dicha configuración contra correo no deseada se almacena en una sección designada para esa cuenta en el perfil del usuario.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816041"
---
# <a name="about-anti-spam-settings"></a>Información sobre la configuración contra correo no deseado

Outlook permite a los usuarios especificar la configuración para cada cuenta para ayudar a proteger la cuenta contra correo no deseado. Dicha configuración contra correo no deseada se almacena en una sección designada para esa cuenta en el perfil del usuario. Utilice la propiedad [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obtener el identificador único (UID) para la sección en el perfil que almacena las preferencias del usuario para esta cuenta, incluida la configuración contra correo no deseada. 
  
Utilice las propiedades siguientes para obtener la configuración contra correo no deseada para la cuenta:
  
- [PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario haya especificado como remitentes bloqueados para la cuenta.
    
- [PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx): especifica el nivel de que el usuario ha especificado para la cuenta de filtrado de correo no deseado. En la siguiente tabla muestra los valores admitidos.
    
|Valores admitidos |Definición |
|:-----|:-----|
|Ninguno  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Medio  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
- [PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como destinatarios de confianza para la cuenta.
    
- [PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como remitentes de confianza para la cuenta.
    
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [Agregar nombres a las listas del filtro de correo electrónico no deseado](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

