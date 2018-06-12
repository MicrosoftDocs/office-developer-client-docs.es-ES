---
title: Estrategias para el tratamiento de errores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820768"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="7d516-103">Estrategias para el tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="7d516-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="7d516-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d516-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d516-105">Debido a que los métodos de interfaz son virtuales, no es posible saber, como autor de la llamada, el conjunto completo de valores que se pueden devolver desde una llamada de prueba.</span><span class="sxs-lookup"><span data-stu-id="7d516-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="7d516-106">Una implementación de un método podría devolver cinco valores; otro podría devolver ocho.</span><span class="sxs-lookup"><span data-stu-id="7d516-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="7d516-107">Lista de las entradas de referencia en la documentación de MAPI unos valores que se pueden devolver para cada método; Estos son los valores que su proveedor de servicio o cliente puede comprobar y controlar porque tienen un significado especial.</span><span class="sxs-lookup"><span data-stu-id="7d516-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="7d516-108">Se pueden devolver otros valores pero, debido a que no están significativas, no es necesario un código especial para controlar estos.</span><span class="sxs-lookup"><span data-stu-id="7d516-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="7d516-109">Una comprobación sencilla para el éxito o el fracaso es la adecuada.</span><span class="sxs-lookup"><span data-stu-id="7d516-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="7d516-110">Algunos de los métodos de interfaz devuelven advertencias.</span><span class="sxs-lookup"><span data-stu-id="7d516-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="7d516-111">Si un método que llama su proveedor de servicio o cliente puede devolver una advertencia, use la macro **HR_FAILED** para probar el valor devuelto en lugar de una comprobación para cero o distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="7d516-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="7d516-112">Advertencias, aunque no es cero, difieren de los códigos de error en que no tienen establecido el bit alto.</span><span class="sxs-lookup"><span data-stu-id="7d516-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="7d516-113">Si su proveedor de cliente o servicio no usa la macro, es probable que podría confundir con una advertencia para un error.</span><span class="sxs-lookup"><span data-stu-id="7d516-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="7d516-114">Aunque la mayoría de los métodos de interfaz y las funciones devuelven valores HRESULT, algunas funciones devuelven valores de tipo long sin signo.</span><span class="sxs-lookup"><span data-stu-id="7d516-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="7d516-115">Además, algunos métodos que se usan en el entorno de MAPI proceden de COM y devuelven los valores de error de COM en lugar de los valores de error MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d516-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="7d516-116">Tenga en cuenta las siguientes instrucciones al realizar llamadas:</span><span class="sxs-lookup"><span data-stu-id="7d516-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="7d516-117">Nunca se basan en o usar los valores devueltos de **IUnknown:: AddRef** o **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="7d516-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="7d516-118">Estos valores devueltos son solo con fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7d516-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="7d516-119">**IUnknown:: QueryInterface** siempre devuelve errores de COM genéricos donde la instalación es FACILITY_NULL o FACILITY_RPC, en lugar de los errores de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d516-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="7d516-120">Todos los otros métodos de interfaz devolución errores de interfaz MAPI con una instalación de FACILITY_ITF o FACILITY_RPC o FACILITY_NULL.</span><span class="sxs-lookup"><span data-stu-id="7d516-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="7d516-121">Cuando se realiza una llamada a un método MAPI no compatible, se puede devolver una de cuatro posibles errores:</span><span class="sxs-lookup"><span data-stu-id="7d516-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="7d516-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7d516-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="7d516-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="7d516-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="7d516-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7d516-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="7d516-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="7d516-125">MAPI_E_VERSION.</span></span> 
  

