---
title: Acción de Macro EjecutarMacro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Puede utilizar la acción EjecutarMacro para ejecutar una macro (UI) de la interfaz de usuario.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815485"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>Acción de Macro EjecutarMacro (aplicación web personalizado de Access)

Puede utilizar la acción **EjecutarMacro** para ejecutar una macro (UI) de la interfaz de usuario. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **EjecutarMacro** utiliza los siguientes argumentos. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
|**Nombre de macro** <br/> |El nombre de la macro de la interfaz de usuario para que se ejecute.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se ejecuta una macro de la interfaz de usuario que contiene la acción **EjecutarMacro** y se llega a la acción **RunMacro (EjecutarMacro)** , Access ejecuta la macro llamada de la interfaz de usuario. Cuando haya terminado la macro llamada de la interfaz de usuario, Access vuelve a la macro de la interfaz de usuario original y ejecuta la siguiente acción. 
  

