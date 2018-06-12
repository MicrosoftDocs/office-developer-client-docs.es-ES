---
title: Acción de Macro DetenerMacro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Puede utilizar la acción DetenerMacro para detener la macro que se está ejecutando.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815491"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>Acción de Macro DetenerMacro (aplicación web personalizado de Access)

Puede utilizar la acción **DetenerMacro** para detener la macro que se está ejecutando. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **DetenerMacro** no tiene ningún argumento. 
  
## <a name="remarks"></a>Notas

Esta acción se suele utilizar cuando una condición haga necesario detener la macro. Por ejemplo, podría crear una macro de usuario (UI) de la interfaz que se abre una vista que muestra los totales de pedidos diarios para la fecha especificada en la vista actual. Podría utilizar una expresión condicional para asegurarse de que el control de fecha de pedido en el cuadro de diálogo contiene una fecha válida. Si no es así, la acción de **cuadro de mensaje** puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro de la interfaz de usuario. 
  

