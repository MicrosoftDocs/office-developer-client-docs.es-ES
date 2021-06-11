---
title: Bloque de datos LookupRecord (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloque de datos BuscarRegistro realiza un conjunto de acciones en un registro específico.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434364"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloque de datos LookupRecord (aplicación web personalizada de Access)

Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
> [!NOTE]
> El bloque de datos **BuscarRegistro** solo está disponible en macros de datos. 
  
## <a name="setting"></a>Configuración

La acción **EstablecerCampo** utiliza los siguientes argumentos. 
  
|**Argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| _In_ <br/> |Sí  <br/> |Una cadena que identifica el registro en el que se operará. El *argumento In* puede contener el nombre de la tabla, una consulta select o una instrucción SQL.  <br/> |
| _Where Condition_ <br/> |No  <br/> |Una expresión de cadena que se utiliza para restringir el intervalo de datos en el que se ejecuta el bloque de datos **BuscarRegistro**. Por ejemplo, los criterios a menudo equivalen a la cláusula WHERE en una expresión SQL, sin la palabra WHERE. Si se omite criteria, el bloque de datos **LookupRecord** funciona en todo el dominio especificado por el *argumento In.* Cualquier campo que se incluya en criteria también debe ser un campo en  *In*  .  <br/> |
| _Alias_ <br/> |No  <br/> |Cadena que proporciona un nombre alternativo para el registro especificado por el *argumento In.* Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas. Si no se especifica  *Alias,*  se usará el nombre de la tabla o consulta como alias.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si los criterios especificados por los argumentos  *En*  y  *Condición WHERE*  especifican más de un registro, el bloque de datos **BuscarRegistro** solo operará en el primer registro. 
  
Si ningún registro satisface *Where Condition* o *si In* no contiene registros, **LookupRecord** crea un registro en blanco en el que todos los campos contienen un **valor Null.** 
  

