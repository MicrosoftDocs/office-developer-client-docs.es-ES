---
title: Información sobre la configuración contra correo no deseado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permite a los usuarios especificar la configuración de cada cuenta para ayudar a proteger la cuenta contra correo no deseado. Esta configuración contra correo no deseado se almacena en una sección designada para esa cuenta en el perfil del usuario.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316964"
---
# <a name="about-anti-spam-settings"></a>Información sobre la configuración contra correo no deseado

Outlook permite a los usuarios especificar la configuración de cada cuenta para ayudar a proteger la cuenta contra correo no deseado. Esta configuración contra correo no deseado se almacena en una sección designada para esa cuenta en el perfil del usuario. Use la [propiedad PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obtener el identificador único (UID) de la sección del perfil que almacena las preferencias del usuario para esta cuenta, incluida la configuración contra correo no deseado. 
  
Use las siguientes propiedades para obtener la configuración contra correo no deseado de la cuenta:
  
- [PidTagSpamJunkSenders:](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como remitentes bloqueados para la cuenta.
    
- [PidTagSpamThreshold:](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)especifica el nivel de filtrado de correo no deseado que el usuario ha especificado para la cuenta. En la tabla siguiente se muestran los valores admitidos.
    
|Valor admitido |Definición |
|:-----|:-----|
|Ninguno  <br/> |0xFFFFFFFF  <br/> |
|Bajo  <br/> |0x00000006  <br/> |
|Medio  <br/> |0x00000005  <br/> |
|Alto  <br/> |0x00000003  <br/> |
   
- [PidTagSpamTrustedRecipients:](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como destinatarios de confianza para la cuenta.
    
- [PidTagSpamTrustedSenders:](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como remitentes de confianza para la cuenta.
    
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [Agregar nombres a las listas de filtro de correo no deseado](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

