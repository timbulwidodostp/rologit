# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Fit RO-logit model and obtain heuristic residuals Use rologit (ROlogit) With R Software
install.packages("ROlogit")
library("ROlogit")
# Estimate Fit RO-logit model and obtain heuristic residuals Use rologit (ROlogit) With R Software
rologit = read.csv("https://raw.githubusercontent.com/timbulwidodostp/rologit/main/rologit/rologit.csv",sep = ";")
rologit$group <- paste(rologit$age_group, rologit$sex, rologit$los_group, rologit$bg_freq_group, sep = "|")
rologit <- rologit(yvar = "bg_mean", evar = "ward", svar = "group", dat = rologit, initial.res.par = c(2, 2))
rologit$obj
rologit$logscale
rologit$coefficients
# Fit RO-logit model and obtain heuristic residuals Use rologit (ROlogit) With R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished