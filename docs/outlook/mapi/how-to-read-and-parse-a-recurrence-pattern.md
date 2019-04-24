---
title: Leer y analizar un patrón de periodicidad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345930"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="eb9f2-103">Leer y analizar un patrón de periodicidad</span><span class="sxs-lookup"><span data-stu-id="eb9f2-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="eb9f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb9f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb9f2-105">MAPI se puede usar para leer y analizar un patrón de periodicidad para una cita.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="eb9f2-106">Para obtener información sobre cómo descargar, ver y ejecutar el código desde el proyecto de aplicación de MFCMAPI al que se hace referencia en este tema, consulte [instalar los ejemplos que se han usado en esta sección](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="eb9f2-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="eb9f2-107">Para analizar un BLOB de periodicidad</span><span class="sxs-lookup"><span data-stu-id="eb9f2-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="eb9f2-108">Abra un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-108">Open an appointment item.</span></span> <span data-ttu-id="eb9f2-109">Para obtener información sobre cómo abrir un mensaje, consulte [abrir un mensaje](opening-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="eb9f2-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="eb9f2-110">Recupere la propiedad con nombre **dispidApptRecur** ([propiedad canónica PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb9f2-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="eb9f2-111">Para obtener información acerca de la recuperación de propiedades con nombre, vea [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="eb9f2-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="eb9f2-112">Siga las instrucciones de [[ms-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) para leer la estructura del patrón de periodicidad de la cita.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-112">Follow the guidance in [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="eb9f2-113">La aplicación de referencia de MFCMAPI muestra el último paso `BinToAppointmentRecurrencePatternStruct` con la función en el archivo de origen de InterpretProp2. cpp del proyecto MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="eb9f2-114">La `BinToAppointmentRecurrencePatternStruct` función toma un puntero a un búfer en la memoria como parámetro.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="eb9f2-115">La aplicación MFCMAPI obtiene este búfer asignando primero la propiedad con nombre **dispidApptRecur** a una etiqueta de propiedad y, a continuación, solicitando el valor de la propiedad mediante el método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9f2-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="eb9f2-116">Si la propiedad es demasiado grande para recuperarla mediante el método **GetProps** , MFCMAPI abre una interfaz de secuencia para recuperar la propiedad mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9f2-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="eb9f2-117">A continuación, la aplicación MFCMAPI Lee los datos fuera de la secuencia para compilar el búfer.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="eb9f2-118">Para obtener información sobre el formato del búfer, vea la [propiedad canónica PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="eb9f2-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="eb9f2-119">La mayor parte de los datos en el búfer consta de campos de un número fijo de bytes, que se deben leer uno tras otro.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="eb9f2-120">Algunos campos solo están presentes si otros campos contienen determinados valores y el tamaño de algunos campos puede depender del valor de otros campos.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="eb9f2-121">El análisis del búfer para leer los distintos campos implica una gran cantidad de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="eb9f2-122">MFCMAPI usa una clase auxiliar interna denominada `CBinaryParser` para encapsular esta contabilidad.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="eb9f2-123">Por ejemplo, la `CBinaryParser::GetDWORD` función comprueba si quedan suficientes bytes en el búfer para leer un DWORD y, a continuación, lee el valor y actualiza los punteros.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="eb9f2-124">Una vez que se ha analizado el búfer en una estructura, la aplicación MFCMAPI `AppointmentRecurrencePatternStructToString` usa la función para convertir la estructura en una cadena que se va a mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="eb9f2-125">Esta no es la misma cadena que Outlook mostraría en su lugar una vista sin formato de los datos en los que Outlook crea su lógica.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="eb9f2-126">Es posible que se encuentre un búfer que contiene datos dañados o más datos de los necesarios para codificar un patrón de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="eb9f2-127">Para ayudar a identificar estos escenarios, la aplicación MFCMAPI realiza un seguimiento de la cantidad de datos que se han analizado correctamente y de la parte que queda en el búfer.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="eb9f2-128">Si los datos permanecen en el búfer después de que se haya completado el análisis, MFCMAPI incluye estos "datos no deseados" en la estructura para poder examinarlos.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="eb9f2-129">A continuación se muestra la lista completa de `BinToAppointmentRecurrencePatternStruct` la función.</span><span class="sxs-lookup"><span data-stu-id="eb9f2-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a><span data-ttu-id="eb9f2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb9f2-130">See also</span></span>

- [<span data-ttu-id="eb9f2-131">Uso de MAPI para crear elementos de Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="eb9f2-131">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

