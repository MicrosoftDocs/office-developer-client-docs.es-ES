---
title: Verbos de formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424031"
---
# <a name="form-verbs"></a>Verbos de formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La interfaz de usuario de un formulario suele ofrecer elementos de menú o controles que permiten a los usuarios realizar algún tipo de acción con el formulario. El trabajo del servidor de formularios controla estas acciones del usuario. Esta interfaz se implementa mediante las API de Win32 estándar; escribir una es igual que escribir otras interfaces para los programas Win32 normales.
  
Con frecuencia, las acciones del usuario están asociadas con verbos. Un verbo es el nombre de una acción específica de una clase de mensaje determinada. Por ejemplo, **reply** es un verbo que implementan varios servidores de formularios, cada uno de los cuales puede tener una interpretación diferente de ese verbo. A veces, los verbos se denominan comandos. 
  
> [!NOTE]
> No todos los elementos de menú y los controles de un formulario corresponden a un verbo. Por ejemplo, un botón **Cancelar** no se corresponde con un verbo de cancelación dentro del servidor de formularios. Normalmente, los verbos están asociados a acciones específicas de una clase de mensaje determinada o un conjunto de clases de mensaje. Aunque diferentes clases de mensaje pueden admitir distintos conjuntos de verbos, todos admiten al menos el verbo abrir, que muestra la interfaz de usuario del formulario y lo carga con los valores de propiedad del mensaje. 
  
Los verbos pueden no tener ningún parámetro. Los formularios que exportan comandos con parámetros de variable deben usar los mecanismos de automatización.
  
Los clientes pueden determinar qué verbos admite una clase de mensaje determinada a través del método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) , implementado por el administrador de formularios MAPI. El administrador de formularios obtiene esta información del archivo de configuración del formulario. El cliente usa el conjunto de verbos devuelto por este método para mostrar al usuario qué comandos se pueden ejecutar en un mensaje. Por ejemplo, es posible que un cliente permita a los usuarios hacer clic con el botón secundario del mouse en un mensaje para mostrar verbos aplicables a ese mensaje. 
  
## <a name="see-also"></a>Ver también

- [Formularios MAPI](mapi-forms.md)

