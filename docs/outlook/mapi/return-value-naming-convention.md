---
title: Devolver Convención de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279828"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="1a4e5-103">Devolver Convención de nomenclatura de valor</span><span class="sxs-lookup"><span data-stu-id="1a4e5-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="1a4e5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a4e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a4e5-105">MAPICODE. H contiene muchos de los valores que un cliente o proveedor de servicios puede devolver desde una implementación de método de interfaz o puede que vea devuelto desde una llamada.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="1a4e5-106">Los códigos que representan las condiciones de advertencia y error siguen una Convención de nomenclatura diferente que comienza con el prefijo MAPI, un guión bajo y una W o una E para indicar el tipo de código.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="1a4e5-107">El resto del código es una cadena de caracteres corta para describir la condición.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="1a4e5-108">Cada palabra de la cadena está separada por un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="1a4e5-109">Por ejemplo, el valor de error MAPI_E_TOO_COMPLEX indica que la implementación no pudo controlar lo que se solicitó en la llamada.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="1a4e5-110">El valor de advertencia MAPI_W_PARTIAL_COMPLETION indica que la llamada se ha realizado correctamente, pero que se han producido problemas.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="1a4e5-111">Solo parte de la operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-111">Only part of the operation was completed successfully.</span></span>
  

