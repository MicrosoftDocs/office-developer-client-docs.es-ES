---
title: Acción de macro GoToControl (aplicación web de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: Puede usar la acción GoToControl para mover el foco al control especificado en el registro actual de la vista abierta.
ms.openlocfilehash: 2368933a6277615554a565d3bdd973f7d1f366f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436478"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>Acción de macro GoToControl (aplicación web de Access)

Puede usar la acción **GoToControl** para mover el foco al control especificado en el registro actual de la vista abierta. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **GoToControl** tiene el siguiente argumento. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
|**Nombre del control** <br/> |El nombre del campo o control donde desea el foco. Este argumento es obligatorio.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar esta acción si desea que un campo o control concreto tenga el foco. También puede usar esta acción para desplazarse por un formulario según ciertas condiciones. Por ejemplo, si el usuario escribe No en un control Casado en un formulario de seguros de salud, el foco puede omitir automáticamente el control Nombre de cónyuge y pasar al siguiente control.
  

