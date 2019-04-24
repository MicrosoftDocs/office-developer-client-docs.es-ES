---
title: Información sobre cómo registrar un nuevo dominio para la configuración automática
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook proporciona una forma de especificar un nuevo dominio del servicio de mensajes para la configuración automática y permitir que el proveedor de servicios de mensajes configure la cuenta.
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316971"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Información sobre cómo registrar un nuevo dominio para la configuración automática

Outlook proporciona una forma de especificar un nuevo dominio del servicio de mensajes para la configuración automática y permitir que el proveedor de servicios de mensajes configure la cuenta.
  
Al diseñar un proveedor de servicios de mensajes, puede usar la siguiente clave en el registro de Windows para especificar un nuevo dominio que el proveedor de servicios de mensajes correspondiente configurará automáticamente: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
En la clave, `<domain name>` es el dominio para la configuración automática. Este nombre de dominio admite un \* comodín solo al principio. En la siguiente tabla se muestran los valores que admite esta clave. 
  
| Valor | Tipo | Descripción |
|:-----|:-----|:-----|
|Nombre descriptivo  <br/> |REG_SZ  <br/> |El nombre de dominio que se muestra al usuario durante la configuración automática.  <br/> |
|Nombre del servicio  <br/> |REG_SZ  <br/> |Servicio de mensajes registrado en MAPISVC. inf que admite este dominio.  <br/> |
|Ubicación de instalación  <br/> |REG_SZ  <br/> |La dirección URL de la ubicación para instalar el proveedor de servicios de mensajes, si aún no está instalado.  <br/> |
|Versión mínima  <br/> |DWORD  <br/> |La versión mínima del archivo. dll del proveedor de servicios de mensajes que se requiere. Este valor es opcional.  <br/> |
   
Cuando Outlook inicia la configuración automática de una cuenta de correo electrónico, comprueba el registro de Windows en busca del registro del dominio especificado por la dirección de correo electrónico. Si el dominio ya está especificado en el registro de Windows, Outlook comprueba si el servicio de mensajes está registrado en MAPISVC. inf. Outlook no puede continuar con la configuración automática del dominio a menos que se haya especificado en el registro de Windows.
  
Si el servicio de mensajes especificado no está actualmente registrado en MAPISVC. inf, o el proveedor de servicios de mensajes está instalado, pero el archivo. dll tiene una versión anterior a la mínima especificada, Outlook usa el nombre descriptivo especificado y solicita al usuario que instale el proveedor. Si el usuario acepta, Outlook redirige al usuario a la ubicación de instalación especificada para que el usuario pueda instalar el proveedor. La instalación del proveedor registra el servicio de mensajes en MAPISVC. inf.
  
Si el servicio de mensajes está actualmente registrado en MAPISVC. inf y el proveedor de servicios. dll es una versión apropiada, Outlook crea el servicio de mensajes con [IMsgServiceAdmin:: CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)y, a continuación, lo [configura mediante IMsgServiceAdmin:: ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). La configuración automática de Outlook usa las tres propiedades siguientes para permitir que el proveedor Configure la cuenta: [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)y [PidTagAutoConfigurationUserPassword ](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Vea también

- [Formato de archivo de MapiSvc. inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

