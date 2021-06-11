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
  
La interfaz de usuario de un formulario normalmente ofrece elementos de menú o controles que permiten a los usuarios realizar algún tipo de acción con el formulario. El trabajo del servidor de formularios es controlar estas acciones de usuario. Esta interfaz se implementa con las API estándar de Win32; escribir uno es igual que escribir otras interfaces para programas win32 normales.
  
A menudo, las acciones del usuario se asocian con verbos. Un verbo es el nombre de una acción específica de una clase de mensaje determinada. Por ejemplo, **Reply** es un verbo implementado por muchos servidores de formulario, cada uno de los cuales puede tener una interpretación diferente de ese verbo. A veces, los verbos se denominan comandos. 
  
> [!NOTE]
> No todos los elementos de menú y los controles de un formulario corresponden a un verbo. Por ejemplo, un **botón Cancelar** no corresponde a un verbo Cancel dentro del servidor de formulario. Normalmente, los verbos se asocian con acciones específicas de una clase de mensaje determinada o un conjunto de clases de mensaje. Aunque diferentes clases de mensaje pueden admitir diferentes conjuntos de verbos, todas admiten al menos el verbo Abrir, que muestra la interfaz de usuario del formulario y la carga con los valores de propiedad del mensaje. 
  
Es posible que los verbos no tomen parámetros. Los formularios que exportan comandos con parámetros variables deben usar los mecanismos de automatización.
  
Los clientes pueden determinar qué verbos son compatibles con una clase de mensaje determinada a través del método [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) que implementa el administrador de formularios MAPI. El administrador de formularios obtiene esta información del archivo de configuración del formulario. El conjunto de verbos devuelto por este método lo usa el cliente para mostrar al usuario qué comandos se pueden ejecutar en un mensaje. Por ejemplo, un cliente puede permitir a los usuarios hacer clic en el botón derecho del mouse sobre un mensaje para mostrar verbos aplicables a ese mensaje. 
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)

