---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use el esquema URI de Sway para abrir la aplicación de Sway y ver o editar un Sway.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415316"
---
# <a name="sway-uri-scheme"></a>Esquema de URI de Sway

Este documento define el formato de los identificadores uniformes de recursos (URI) de la aplicación de Sway para Windows. Puede usar este esquema de URI para invocar la aplicación de Sway con varios comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxis de esquema URI de Sway

A continuación se encuentra la sintaxis del esquema URI:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indica que Sway es la aplicación que se va a invocar. Cuando Sway para Windows está instalado, `ms-sway` se registra con Windows como el controlador de Sway.
- `<command-argument>`&ndash; Un URI puede tener uno o varios argumentos de comando, delimitados por el`&`carácter y comercial (). Cuando se incluye más de un argumento de comando en un identificador URI, el`&`carácter "y" comercial () debe separar cada argumento de comando del siguiente argumento de comando. Los argumentos del comando varían según el escenario. 

## <a name="command-arguments"></a>Argumentos de comando

Se pueden incluir varios argumentos de comando como parte del esquema de dirección URL de Sway. Estos argumentos de comando no son necesarios. Si no incluye los argumentos del comando, se invoca la aplicación de Sway.

|Nombre del argumento de comando|Descripción|Tipo|Valores posibles|¿Necesario?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|El identificador único de un Sway. Se usa para indicar el Sway que se va a abrir.|Cadena|Un identificador único válido para un Sway. El identificador siempre forma parte de la dirección URL de un Sway.<br/><br/>Por ejemplo, para el siguiente Sway `https://sway.com/dBheQgVZ1RQBfiQU`, el identificador es `dBheQgVZ1RQBfiQU`.<br/><br/>Si la cuenta de usuario asociada a la aplicación de Sway tiene permisos de edición, la aplicación abre el Sway en el modo de edición. De lo contrario, la aplicación abre el Sway en el modo de visualización.|No|
|**mode**|Modo en el que se debe abrir un Sway específico, ya sea para su edición o para su visualización.|Cadena|edit<br/>vista<br/><br/>**Nota**: Si no se especifica ningún **identificador** , se omite este argumento de comando.|No|
|**auth_upn**|La cuenta que se usará al abrir Sway.|Cadena|Una dirección de correo electrónico válida.<br/><br/>Si la dirección de correo electrónico especificada no está asociada a una cuenta de Sway, Sway le pedirá al usuario que inicie sesión como el usuario especificado.<br/><br/>Si hay más de una cuenta asociada a la aplicación de Sway y la dirección de correo electrónico especificada existe, la aplicación de Sway cambia a usar esa cuenta cuando se invoca.|No|
|**auth\_PVR**|El tipo de cuenta que se va a usar para&mdash;abrir Sway, ya sea una cuenta de Microsoft o una cuenta de Azure Active Directory (Azure ad).|Cadena|WindowsLiveId: especifica que la cuenta de **UPN de autenticación\_** es una cuenta de Microsoft.<br/><br/>OrgId: especifica que la cuenta de **UPN de autenticación\_** es una cuenta de Azure ad.<br/><br/>Si no se especifica ningún **UPN de autenticación\_** , se omite este argumento de comando.|No|
|**invocar\_aplicación**|El nombre de la aplicación de Windows que se usa para invocar Sway.|Cadena|El nombre descriptivo de la aplicación para Windows que se usa para invocar Sway mediante el esquema de dirección URL de Sway.<br/><br/>El propósito de este argumento de comando es para telemetría y seguimiento.|No|

## <a name="uri-scheme-semantics"></a>Semántica del esquema URI

El `<ms-sway>` esquema define una sintaxis URI para abrir un Sway o para invocar la aplicación de Sway. El esquema define varios argumentos de comando, que se pueden usar para hacer lo siguiente: 

- Abrir la aplicación &ndash; de Sway no es necesario especificar ningún argumento de comando. 

- Abrir un Sway para verlo en la aplicación &ndash; de Sway el **identificador** y el **modo** establecidos para la vista deben especificarse. 

- Abrir un Sway para editarlo en la aplicación &ndash; de Sway el **identificador** y el **modo** establecidos para la edición deben especificarse. También se recomienda incluir el **UPN de\_autenticación** y **los\_PVR de autenticación** para ayudar a garantizar que se use la cuenta correcta con permisos de edición cuando se abra Sway.  

## <a name="example"></a>Ejemplo

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


