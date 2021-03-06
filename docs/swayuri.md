---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use el esquema uri de Sway para abrir la aplicación Sway y ver o editar un Sway.
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415316"
---
# <a name="sway-uri-scheme"></a>Esquema de URI de Sway

Este documento define el formato de identificadores uniformes de recursos (URI) para la aplicación Sway para Windows. Puede usar este esquema uri para invocar la aplicación Sway con varios comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxis de esquema URI de Sway

A continuación se muestra la sintaxis del esquema URI:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash;Indica que Sway es la aplicación que se va a invocar. Cuando Sway para Windows está instalado, se registra `ms-sway` con Windows para ser el controlador Sway.
- `<command-argument>`&ndash;Un URI puede tener uno o varios argumentos de comando, delimitados por el carácter ampersand ( `&` ). Cuando se incluye más de un argumento de comando en un URI, un carácter ampersand ( ) debe separar cada argumento de comando `&` del siguiente argumento de comando. Los argumentos de comando varían según el escenario. 

## <a name="command-arguments"></a>Argumentos command

Se pueden incluir varios argumentos de comando como parte del esquema de dirección URL de Sway. Estos argumentos de comando no son necesarios. Si no incluye los argumentos de comando, se invoca la aplicación Sway.

|Nombre del argumento Command|Descripción|Tipo|Valores posibles|¿Necesario?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|El identificador único de un Sway. Se usa para indicar el Sway que se va a abrir.|Cadena|Un identificador único válido para un Sway. El identificador siempre forma parte de la dirección URL de un Sway.<br/><br/>Por ejemplo, para el siguiente Sway `https://sway.com/dBheQgVZ1RQBfiQU` , el identificador es `dBheQgVZ1RQBfiQU` .<br/><br/>Si la cuenta de usuario asociada a la aplicación Sway tiene permisos de edición, la aplicación abre Sway en modo de edición. De lo contrario, la aplicación abre el Sway en modo de vista.|No|
|**mode**|Modo en el que se debe abrir un Sway específico, ya sea para edición o para visualización.|Cadena|edit<br/>vista<br/><br/>**NOTA**: Si no se especifica ningún **identificador,** se omite este argumento de comando.|No|
|**auth_upn**|Cuenta que se va a usar al abrir Sway.|Cadena|Una dirección de correo electrónico válida.<br/><br/>Si la dirección de correo electrónico especificada no está asociada a una cuenta de Sway, Sway pide al usuario que inicie sesión como el usuario especificado.<br/><br/>Si hay más de una cuenta asociada a la aplicación Sway y existe la dirección de correo electrónico especificada, la aplicación Sway cambia a usar esa cuenta cuando se invoca.|No|
|**pvr \_ de autenticación**|Tipo de cuenta que se va a usar para abrir la cuenta de Sway, ya sea una cuenta de Microsoft o una cuenta Azure Active Directory &mdash; (Azure AD).|Cadena|WindowsLiveId: especifica que la **cuenta de \_ autenticación upn** es una cuenta de Microsoft.<br/><br/>OrgId: especifica que la **cuenta de \_ autenticación upn** es una cuenta de Azure AD.<br/><br/>Si no **se especifica \_ ningún upn** de autenticación, se omite este argumento de comando.|No|
|**invocar \_ aplicación**|Nombre de la aplicación Windows que se usa para invocar Sway.|Cadena|Nombre descriptivo de la aplicación Windows que se usa para invocar Sway a través del esquema de dirección URL de Sway.<br/><br/>El propósito de este argumento de comando es la telemetría y el seguimiento.|No|

## <a name="uri-scheme-semantics"></a>Semántica de esquema URI

El `<ms-sway>` esquema define una sintaxis uri para abrir un Sway o para invocar la aplicación Sway. El esquema define varios argumentos de comando, que se pueden usar para hacer lo siguiente: 

- Abra la aplicación Sway No es necesario especificar &ndash; argumentos de comando. 

- Abrir un Sway para su visualización en la aplicación Sway Es necesario especificar el identificador y el modo &ndash; establecidos para  ver.  

- Abrir un Sway para su edición en la aplicación Sway Es necesario especificar el identificador y el modo &ndash; establecidos para  editar.  Se recomienda incluir también **auth \_ upn** y **auth \_ pvr** para garantizar que la cuenta correcta con permisos de edición se usa cuando se abre Sway.  

## <a name="example"></a>Ejemplo

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


