---
title: Función CharIndex (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Las búsquedas que se encuentra una expresión de texto para otra expresión de texto y devuelve su inicio posición si.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815345"
---
# <a name="charindex-function-access-custom-web-app"></a>Función CharIndex (aplicación web personalizado de Access)

Las búsquedas que se encuentra una expresión de texto para otra expresión de texto y devuelve su inicio posición si.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**CharIndex** (*TextExpression*, *WithinText*, [*Iniciar*]) 
  
|**Nombre del argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Sí  <br/> |Una expresión de texto que contiene el texto que se encuentra.  <br/> |
| *WithinText*  <br/> |Sí  <br/> |La expresión de texto que se desea buscar.  <br/> |
| *Start*  <br/> |No  <br/> |Un entero que especifica la ubicación en *WithinText* para iniciar la búsqueda. Si *Iniciar* no se especifica, es un número negativo o es 0, la búsqueda comienza al principio de *WithinText* .  <br/> |
   
## <a name="remarks"></a>Comentarios

Si *TextExpression* o *WithinText* es NULL, *CharIndex* devuelve NULL. 
  
Si no se encuentra *TextExpression* dentro de *WithinText*, *CharIndex* devuelve 0. 
  
La posición inicial devuelta está basado en 1, no en 0.
  

