---
title: Información sobre cómo registrar un nuevo dominio para la configuración automática
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook proporciona una forma de especificar un nuevo dominio de servicio de mensajes para la configuración automática y permitir que el proveedor de servicios de mensajes configure la cuenta.
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316971"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Información sobre cómo registrar un nuevo dominio para la configuración automática

Outlook proporciona una forma de especificar un nuevo dominio de servicio de mensajes para la configuración automática y permitir que el proveedor de servicios de mensajes configure la cuenta.
  
Al diseñar un proveedor de servicios de mensajes, puede usar la siguiente clave en el Registro de Windows para especificar un nuevo dominio que configurará automáticamente el proveedor de servicios de mensajes correspondiente: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
En la clave, `<domain name>` está el dominio para la configuración automática. Este nombre de dominio solo admite un comodín \* al principio. En la tabla siguiente se muestran los valores que admite esta clave. 
  
| Valor | Tipo | Descripción |
|:-----|:-----|:-----|
|Nombre descriptivo  <br/> |REG_SZ  <br/> |Nombre de dominio que se muestra al usuario durante la configuración automática.  <br/> |
|Nombre del servicio  <br/> |REG_SZ  <br/> |El servicio de mensajes registrado en mapisvc.inf que admite este dominio.  <br/> |
|Ubicación de instalación  <br/> |REG_SZ  <br/> |Dirección URL de la ubicación para instalar el proveedor de servicios de mensajes, si aún no está instalada.  <br/> |
|Versión mínima  <br/> |REG_DWORD  <br/> |La versión mínima del .dll del proveedor de servicios de mensajes que es necesario. Este valor es opcional.  <br/> |
   
Cuando Outlook la configuración automática de una cuenta de correo electrónico, comprueba el registro Windows el registro del dominio especificado por la dirección de correo electrónico. Si el dominio ya está especificado en el Windows, Outlook comprueba si el servicio de mensajes está registrado en Mapisvc.inf. Outlook puede continuar con la configuración automática del dominio a menos que se haya especificado en el Windows registro.
  
Si el servicio de mensajes especificado no está registrado actualmente en Mapisvc.inf o el proveedor de servicios de mensajes está instalado, pero el .dll tiene una versión anterior al mínimo especificado, Outlook usa el nombre descriptivo especificado y solicita al usuario que instale el proveedor. Si el usuario acepta, Outlook redirige al usuario a la ubicación de instalación especificada para que el usuario pueda instalar el proveedor. Al instalar el proveedor, se registra el servicio de mensajes en Mapisvc.inf.
  
Si el servicio de mensajes está registrado actualmente en Mapisvc.inf y el proveedor de servicios .dll es una versión adecuada, Outlook crea el servicio de mensajes mediante [IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)y, a continuación, lo configura mediante [IMsgServiceAdmin::ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Outlook configuración automática usa las tres propiedades siguientes para permitir al proveedor configurar la cuenta: [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)y [PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Vea también

- [Formato de archivo mapiSvc.inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

