---
title: Función concat (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815302"
---
# <a name="concat-function-access-custom-web-app"></a>Función concat (aplicación web personalizado de Access)

Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Syntax

**Concat** (*Valor1*, *valor2*... [*ValorN*]) 
  
La función **Concat** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Description**|
|:-----|:-----|
|Value  <br/> |Un valor de cadena que se concatena a los otros valores.  <br/> |
   
## <a name="remarks"></a>Remarks

**Concat** toma un número variable de argumentos de cadena y los concatena en una sola cadena. Se necesitan, como mínimo, dos argumentos de cadena; si no, se produce un error. 
  
Todos los argumentos se convierten implícitamente en tipos de datos de cadena y luego se concatenan.
  
## <a name="example"></a>Example

La siguiente expresión puede usarse para mostrar el nombre completo de una persona cuando la tabla contiene los campos Nombre, Inicial intermedia y Apellidos. Si el campo MiddleInitial está en blanco, se combinan los campos FirstName y LastName (apellidos) para mostrar el nombre completo.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


