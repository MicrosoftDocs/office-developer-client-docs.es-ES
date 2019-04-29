---
title: Acción de macro RunMacro (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Puede usar la acción EjecutarMacro para ejecutar una macro de interfaz de usuario (UI).
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438445"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>Acción de macro RunMacro (aplicación web personalizada de Access)

Puede usar la acción **EjecutarMacro** para ejecutar una macro de interfaz de usuario (UI). 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **EjecutarMacro** utiliza los siguientes argumentos. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
|**Nombre de macro** <br/> |Nombre de la macro de interfaz de usuario que se va a ejecutar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se ejecuta una macro de interfaz de usuario que contiene la acción **EjecutarMacro** y se alcanza la acción **EjecutarMacro** , Access ejecuta la macro de interfaz de usuario llamada. Cuando la macro de interfaz de usuario llamada ha finalizado, Access vuelve a la macro de interfaz de usuario original y ejecuta la siguiente acción. 
  

