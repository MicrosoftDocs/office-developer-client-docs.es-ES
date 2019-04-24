---
title: SetField (acción de macro) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: La acción EstablecerCampo puede utilizarse para asignar un valor a un campo.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307900"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>SetField (acción de macro) (aplicación web personalizada de Access)

La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> La acción **EstablecerCampo** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Configuración

La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Una cadena que identifica el campo.  <br/> |
|**Value** <br/> |Una expresión que especifica el valor que se va a asignar al campo.  <br/> |
   
## <a name="remarks"></a>Comentarios

La acción **SetField** no se puede usar fuera de un bloque de datos **[CrearRegistro](createrecord-data-block-access-custom-web-app.md)** o **[EditarRegistro](editrecord-data-block-access-custom-web-app.md)** . 
  

