---
title: Función Concat (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423275"
---
# <a name="concat-function-access-custom-web-app"></a>Función Concat (aplicación web personalizada de Access)

Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

**Concat**(*Valor1*, *Valor2*, …[*ValorN*]) 
  
La función **Concat** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
|Valor  <br/> |Un valor de cadena que se concatena a los otros valores.  <br/> |
   
## <a name="remarks"></a>Comentarios

**Concat** toma un número variable de argumentos de cadena y los concatena en una sola cadena. Se necesitan, como mínimo, dos argumentos de cadena; si no, se produce un error. 
  
Todos los argumentos se convierten implícitamente en tipos de datos de cadena y luego se concatenan.
  
## <a name="example"></a>Ejemplo

La siguiente expresión puede usarse para mostrar el nombre completo de una persona en la tabla que contiene los campos Nombre, Segundo nombre y Apellidos. Si el campo Segundo nombre está en blanco, los campos Nombre y Apellidos se combinan para mostrar el nombre completo,
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


