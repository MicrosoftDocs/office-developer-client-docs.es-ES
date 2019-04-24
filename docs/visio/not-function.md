---
title: NOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Devuelve TRUE (1) si expresiónLógica es FALSE. De lo contrario, devuelve FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341143"
---
# <a name="not-function"></a>Función NOT

Devuelve TRUE (1) si _expresiónLógica_ es false. De lo contrario, devuelve FALSE (0). 
  
## <a name="syntax"></a>Sintaxis

NOT (* * *expresiónLógica* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresiónLógica_ <br/> |Obligatorio  <br/> |**String** <br/> |La expresión lógica por evaluar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="example"></a>Ejemplo

NO (altura \> 0,75 de) 
  
Devuelve 1 si Height es menor o igual que 0,75 pulgadas. Devuelve 0 si Height es mayor que 0,75 pulgadas. 
  

