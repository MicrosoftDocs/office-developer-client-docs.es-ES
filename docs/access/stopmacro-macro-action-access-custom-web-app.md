---
title: DetenerMacro (acción de macro) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Puede usar la acción DetenerMacro para detener la macro que se está ejecutando actualmente.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429498"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>DetenerMacro (acción de macro) (aplicación web personalizada de Access)

Puede usar la acción **DetenerMacro** para detener la macro que se está ejecutando actualmente. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La **acción DetenerMacro** no tiene argumentos. 
  
## <a name="remarks"></a>Comentarios

Normalmente, esta acción se usa cuando una condición hace que sea necesario detener la macro. Por ejemplo, puede crear una macro de interfaz de usuario (UI) que abra una vista que muestre los totales del orden diario de la fecha especificada en la vista actual. Puede usar una expresión condicional para asegurarse de que el control Fecha de pedido del cuadro de diálogo contiene una fecha válida. Si no lo hace, la acción **CuadroDe** Mensaje puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro de interfaz de usuario. 
  

