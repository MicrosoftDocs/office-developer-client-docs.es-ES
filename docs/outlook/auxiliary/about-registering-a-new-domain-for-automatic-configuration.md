---
title: Acerca de cómo registrar un nuevo dominio para la configuración automática
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook proporciona una forma para especificar un nuevo dominio de servicio de mensaje para la configuración automática y permitir que el proveedor de servicios de mensaje configurar la cuenta.
ms.openlocfilehash: c1daea81fe18e5d1088a233a3fcdff076419d6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816055"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Acerca de cómo registrar un nuevo dominio para la configuración automática

Outlook proporciona una forma para especificar un nuevo dominio de servicio de mensaje para la configuración automática y permitir que el proveedor de servicios de mensaje configurar la cuenta.
  
Al diseñar un proveedor de servicios de mensaje, puede usar la siguiente clave en el registro de Windows para especificar un nuevo dominio a configurarse automáticamente por el proveedor de servicios de mensaje correspondiente: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
En la clave `<domain name>` es el dominio para la configuración automática. Este nombre de dominio es compatible con un carácter comodín \* al principio sólo. En la siguiente tabla muestra los valores que admite esta clave. 
  
| Valor | Tipo | Descripción |
|:-----|:-----|:-----|
|Nombre descriptivo  <br/> |REG_SZ  <br/> |El nombre de dominio que se muestra al usuario durante la configuración automática.  <br/> |
|Nombre de servicio  <br/> |REG_SZ  <br/> |El servicio de mensajes registrado en mapisvc.inf que admite este dominio.  <br/> |
|Ubicación de instalación  <br/> |REG_SZ  <br/> |La dirección URL de la ubicación para instalar al proveedor de servicios de mensaje, si aún no está instalado.  <br/> |
|Versión mínima  <br/> |REG_DWORD  <br/> |La versión mínima de la DLL del proveedor de servicios de mensaje que es necesario. Este valor es opcional.  <br/> |
   
Cuando Outlook comienza la configuración automática de una cuenta de correo electrónico, comprueba el registro de Windows para el registro del dominio especificado por la dirección de correo electrónico. Si el dominio ya está especificado en el registro de Windows, Outlook comprueba si el servicio de mensajes está registrado en Mapisvc.inf. Outlook no puede continuar con la configuración automática del dominio a menos que se ha especificado en el registro de Windows.
  
Si el servicio de mensaje especificado no está registrado actualmente en Mapisvc.inf, o el proveedor de servicios de mensaje está instalado, pero el archivo .dll tiene una versión anterior al mínimo especificado, Outlook usa el nombre descriptivo especificado y solicita al usuario que instale el proveedor. Si el usuario acepta, Outlook redirige al usuario a la ubicación de instalación especificada para que el usuario puede instalar al proveedor. Instalar al proveedor, registra el servicio de mensajes en Mapisvc.inf.
  
Si el servicio de mensajes está actualmente registrado en Mapisvc.inf y el archivo .dll de proveedor de servicio es una versión apropiada, crea el servicio de mensajes mediante el uso de [IMsgServiceAdmin::](http://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)Outlook y, a continuación, configura mediante el uso de [ IMsgServiceAdmin::ConfigureMsgService](http://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Configuración automática de Outlook usa las tres propiedades siguientes para permitir que el proveedor que se va a configurar la cuenta: [PidTagAutoConfigurationUserName](http://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](http://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)y [PidTagAutoConfigurationUserPassword ](http://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Ver también

- [Formato de archivo de MapiSvc.inf](http://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

