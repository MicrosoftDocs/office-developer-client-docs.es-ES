---
title: Estrategias para el control de errores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424150"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="49741-103">Estrategias para el control de errores</span><span class="sxs-lookup"><span data-stu-id="49741-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="49741-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49741-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49741-105">Dado que los métodos de interfaz son virtuales, no es posible conocer, como autor de la llamada, el conjunto completo de valores que se pueden devolver desde una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="49741-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="49741-106">Una implementación de un método puede devolver cinco valores; otro podría devolver ocho.</span><span class="sxs-lookup"><span data-stu-id="49741-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="49741-107">Las entradas de referencia de la documentación mapi enumera algunos valores que se pueden devolver para cada método; estos son los valores que el cliente o el proveedor de servicios pueden comprobar y controlar porque tienen significados especiales.</span><span class="sxs-lookup"><span data-stu-id="49741-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="49741-108">Se pueden devolver otros valores, pero como no son significativos, el código especial para controlar esos valores no es necesario.</span><span class="sxs-lookup"><span data-stu-id="49741-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="49741-109">Una comprobación sencilla de si se ha hecho correctamente o no es suficiente.</span><span class="sxs-lookup"><span data-stu-id="49741-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="49741-110">Algunos de los métodos de interfaz devuelven advertencias.</span><span class="sxs-lookup"><span data-stu-id="49741-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="49741-111">Si un método al que llama el cliente o el proveedor de servicios puede devolver una advertencia, use la macro **HR_FAILED** para probar el valor devuelto en lugar de comprobar cero o distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="49741-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="49741-112">Las advertencias, aunque distintas de cero, difieren de los códigos de error en que no tienen el conjunto de bits alto.</span><span class="sxs-lookup"><span data-stu-id="49741-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="49741-113">Si su cliente o proveedor de servicios no usa la macro, es probable que una advertencia se pueda confundir con un error.</span><span class="sxs-lookup"><span data-stu-id="49741-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="49741-114">Aunque la mayoría de los métodos y funciones de interfaz devuelven valores HRESULT, algunas funciones devuelven valores largos sin signo.</span><span class="sxs-lookup"><span data-stu-id="49741-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="49741-115">Además, algunos métodos usados en el entorno MAPI provienen de COM y devuelven valores de error COM en lugar de valores de error MAPI.</span><span class="sxs-lookup"><span data-stu-id="49741-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="49741-116">Tenga en cuenta las siguientes directrices al realizar llamadas:</span><span class="sxs-lookup"><span data-stu-id="49741-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="49741-117">Nunca confíe ni use los valores devueltos de **IUnknown::AddRef** o **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="49741-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="49741-118">Estos valores devueltos son solo para fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="49741-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="49741-119">**IUnknown::QueryInterface** siempre devuelve errores COM genéricos donde la instalación FACILITY_NULL o FACILITY_RPC, en lugar de errores MAPI.</span><span class="sxs-lookup"><span data-stu-id="49741-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="49741-120">Todos los demás métodos de interfaz devuelven errores de interfaz MAPI con una FACILITY_ITF de FACILITY_RPC o FACILITY_NULL errores.</span><span class="sxs-lookup"><span data-stu-id="49741-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="49741-121">Cuando se realiza una llamada a un método MAPI no compatible, se puede devolver uno de los cuatro errores posibles:</span><span class="sxs-lookup"><span data-stu-id="49741-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="49741-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="49741-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="49741-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="49741-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="49741-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49741-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="49741-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="49741-125">MAPI_E_VERSION.</span></span> 
  

