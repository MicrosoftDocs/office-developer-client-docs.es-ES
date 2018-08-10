---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Use el esquema de URI influir hora de elegir para abrir la aplicación de balanceo y ver o editar un balanceo.
ms.openlocfilehash: 7a820339abcd666e7e1b9ad584cd152ca8fd4f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821507"
---
# <a name="sway-uri-scheme"></a>Esquema de URI de Sway

Este documento define el formato de identificadores uniformes de recursos (URI) de la aplicación de balanceo para Windows. Puede utilizar este esquema de URI para invocar la aplicación de balanceo con diversos comandos.

## <a name="sway-uri-scheme-syntax"></a>Sintaxis de esquema URI influir la hora de elegir

La siguiente es la sintaxis de esquema URI:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Indica que balanceo es la aplicación que se invoca. Cuando se instala influir hora de elegir para Windows, `ms-sway` está registrado con Windows para que el controlador de balanceo.
- `<command-argument>`&ndash; Un URI puede tener uno o más argumentos del comando, delimitados por la y comercial (`&`) caracteres. Cuando se incluye más de un argumento de comando en un identificador URI, una y comercial (`&`) carácter debe separar cada argumento de comando desde el siguiente argumento de comando. Argumentos de comando varían según el escenario. 

## <a name="command-arguments"></a>Argumentos de comando

Varios argumentos de comando pueden incluirse como parte de la combinación de dirección URL influir hora de elegir. Estos argumentos de comando no son necesarios. Si no se incluyen los argumentos de comando, se invoca la aplicación balanceo.

|Nombre del argumento de comando|Descripción|Tipo|Valores posibles|¿Obligatorio?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|El identificador único de un balanceo. Se usa para indicar el balanceo va a abrir.|String|Un identificador único válido para un balanceo. El identificador siempre es parte de la dirección URL a un balanceo.<br/><br/>Por ejemplo, para el siguiente balanceo `https://sway.com/dBheQgVZ1RQBfiQU`, el identificador es `dBheQgVZ1RQBfiQU`.<br/><br/>Si la cuenta de usuario asociada a la aplicación de balanceo tiene permisos de edición, la aplicación abre el balanceo en modo de edición. De lo contrario, la aplicación abre el balanceo en modo de vista.|No|
|**mode**|El modo en que se debe abrir un balanceo específico si para su edición o para su visualización.|String|edit<br/>vista<br/><br/>**Nota**: si no se especifica ningún **identificador** , se omite este argumento de comando.|No|
|**auth_upn**|La cuenta que se utilizará al abrir balanceo.|String|Una dirección de correo electrónico válida.<br/><br/>Si la dirección de correo electrónico especificada no está asociada con una cuenta de balanceo, balanceo pregunta al usuario para iniciar sesión como el usuario especificado.<br/><br/>Si más de una cuenta está asociada con la aplicación de balanceo y la dirección de correo electrónico especificada existe, la aplicación de balanceo pasa a utilizar esa cuenta cuando se invoca.|No|
|**AUTH\_pvr**|El tipo de cuenta que se va a usar para abrir el balanceo&mdash;una cuenta de Microsoft o una cuenta de Azure Active Directory (AD Azure).|String|WindowsLiveId – especifica que la **auth\_upn** cuenta es una cuenta de Microsoft.<br/><br/>OrgId – especifica que la **auth\_upn** cuenta es una cuenta de Azure AD.<br/><br/>Si no hay **auth\_upn** se especifica, se omite este argumento de comando.|No|
|**invocar\_aplicación**|El nombre de la aplicación de Windows que se usa para invocar balanceo.|String|El nombre descriptivo de la aplicación de Windows que se usa para invocar balanceo a través de la combinación de dirección URL influir hora de elegir.<br/><br/>El propósito de este argumento de comando es para telemetría y seguimiento.|No|

## <a name="uri-scheme-semantics"></a>Semántica de esquema URI

El `<ms-sway>` scheme define una sintaxis URI para abrir un balanceo o para invocar la aplicación de balanceo. El esquema define varios argumentos de comando, que se pueden usar para hacer lo siguiente: 

- Abra la aplicación de balanceo &ndash; no necesitan especificarse argumentos de comando. 

- Abra un balanceo para su visualización en la aplicación de balanceo &ndash; es necesario especificar el **identificador** y el **modo** establecido para ver. 

- Abra un balanceo para su edición en la aplicación de balanceo &ndash; el **identificador** y el **modo de** establecen para editar las necesidades que se especifique. Se recomienda incluir también **auth\_upn** y **auth\_pvr** para ayudar a garantizar que el derecha cuenta con permisos de edición se usa cuando se abre balanceo.  

## <a name="example"></a>Ejemplo

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


