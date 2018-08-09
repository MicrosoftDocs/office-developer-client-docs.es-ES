---
title: Acción de Macro SetField (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: La acción EstablecerCampo puede utilizarse para asignar un valor a un campo.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815492"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>Acción de Macro SetField (aplicación web personalizado de Access)

La acción **EstablecerCampo** puede utilizarse para asignar un valor a un campo. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> [!NOTA] La acción **EstablecerCampo** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Valores

La acción **EstablecerCampo** utiliza los argumentos enumerados en la tabla siguiente. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Una cadena que identifica el campo.  <br/> |
|**Valor** <br/> |Una expresión que especifica el valor que se asigna al campo.  <br/> |
   
## <a name="remarks"></a>Comentarios

No se puede usar la acción **EstablecerCampo** fuera de un bloque de datos **[CrearRegistro](createrecord-data-block-access-custom-web-app.md)** o **[EditarRegistro](editrecord-data-block-access-custom-web-app.md)** . 
  

