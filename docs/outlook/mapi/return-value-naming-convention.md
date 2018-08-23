---
title: Devolver convención de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581849"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="e1c9c-103">Devolver convención de nomenclatura de valor</span><span class="sxs-lookup"><span data-stu-id="e1c9c-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="e1c9c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1c9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1c9c-105">El MAPICODE. Archivo de encabezado de H contiene muchos de los valores que un proveedor de cliente o servicio podría devolver desde una implementación de método de interfaz o es posible que vea devuelto desde una llamada.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="e1c9c-106">Los códigos que representan las condiciones de error y advertencia siguen una convención de nomenclatura diferente que comienza con el prefijo de MAPI, un carácter de subrayado y una W o una E para indicar el tipo de código.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="e1c9c-107">El resto del código es una cadena corta de caracteres para describir la condición.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="e1c9c-108">Cada palabra en la cadena viene separada por un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="e1c9c-109">Por ejemplo, el valor de error MAPI_E_TOO_COMPLEX indica que la implementación no pudo controlar lo que se solicitó en la llamada.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="e1c9c-110">El valor de advertencia MAPI_W_PARTIAL_COMPLETION indica que la llamada se ha realizado correctamente, pero que se han producido problemas.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="e1c9c-111">Sólo una parte de la operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1c9c-111">Only part of the operation was completed successfully.</span></span>
  

