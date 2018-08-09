---
title: Elija función (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Devuelve el elemento en el índice especificado de una lista de valores.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815328"
---
# <a name="choose-function-access-custom-web-app"></a>Elija función (aplicación web personalizado de Access)

Devuelve el elemento en el índice especificado de una lista de valores.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**Elija** (*NúmeroDeÍndice*, *valor*, [*Value_n*]) 
  
La función **Choose** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *NúmeroDeÍndice*  <br/> |Una expresión de número entero que representa un índice basado en 1 en la lista de los elementos a continuación del mismo.  <br/> |
| *Valor*  <br/> |Lista de valores de cualquier tipo de datos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la proporcionada *númeroDeÍndice* no es un entero, el valor se convierte implícitamente a un valor entero. 
  
Si el valor de índice supera los límites de la matriz de valores, **Choose** devuelve NULL. 
  

