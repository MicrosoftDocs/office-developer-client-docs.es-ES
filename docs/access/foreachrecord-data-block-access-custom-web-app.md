---
title: Bloque de datos ParaCadaRegistro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloque de datos ParaCadaRegistro repite un conjunto de instrucciones para cada registro en un dominio.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815344"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloque de datos ParaCadaRegistro (aplicación web personalizado de Access)

Un bloque de datos **ParaCadaRegistro** repite un conjunto de instrucciones para cada registro en un dominio. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> [!NOTA] El bloque de datos **ParaCadaRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Valores

La acción **ParaCadaRegistro** utiliza los siguientes argumentos. 
  
|**Nombre del argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
|**En ** <br/> |Sí  <br/> |Una cadena que identifica el dominio de registros que se va a funcionar en. El argumento *en* puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.  <br/> **Nota**: el dominio especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.           |
|**Where Condition** <br/> |No  <br/> |Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos **ParaCadaRegistro** se lleva a cabo. Por ejemplo, criterios con frecuencia es equivalente a la cláusula WHERE en una expresión SQL, sin la palabra donde. Si se omiten criterios, el bloque de datos **ParaCadaRegistro** funciona en todo el dominio especificado por el argumento *en* . Cualquier campo que se incluya en criterios debe ser también un campo de *en* .  <br/> |
|**Alias** <br/> |No  <br/> |Una cadena que proporciona un nombre alternativo para el dominio especificado por el argumento *en* . A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica el *Alias* , se usará el nombre de la tabla o consulta como el alias.  <br/> |
   
## <a name="remarks"></a>Comentarios

Utilice la acción **[SalirDeCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para salir inmediatamente de un bloque de datos **ParaCadaRegistro**. 
  

